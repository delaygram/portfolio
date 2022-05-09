# 1. Inhoud
- [1. Inhoud](#1-inhoud)
- [2. Document historie](#2-document-historie)
- [3. Introductie](#3-introductie)
- [4. Stappen](#4-stappen)
  - [4.1. feature/**](#41-feature)
  - [4.2. development](#42-development)
  - [4.3. main](#43-main)
- [5. Conclusie](#5-conclusie)

# 2. Document historie

| Versie | Veranderingen                                                                                  | Datum      |
| -----: | ---------------------------------------------------------------------------------------------- | ---------- |
|    0.1 | Eerste opzet document                                                                          | 19-04-2022 |
|    0.2 | Verschillende pipelines beschrijvingen toegevoegd                                              | 19-04-2022 |

# 3. Introductie

Met dit document wil ik bewijzen dat ik een fatsoenlijke CI/CD pipeline op kan zetten met de benodigde onderdelen om ervoor te zorgen dat alleen kwaliteit wordt opgeleverd naar de cloud services toe.

Voorheen is er voornamelijk bezig geweest met het gebruik van Jenkins en Jenkins pipelines, echter is de kennis van GitHub Actions nog redelijk summier waarbij dit semester de bedoeling is om de kennis hiervan uit te breiden tot een volwaardig niveau.

# 4. Stappen

Om een pipeline op te kunnen zetten is het de bedoeling dat in de folder `.github/workflows` een `yml` bestand wordt neergezet met een passende naam.

In een pipeline moeten veel onderdelen meegenomen worden om uiteindleijk een volwaardig product te hebben, zo zijn de pipelines ook verdeeld in verschillende branches. Er zijn pipelines opgezet op de volgende branches:

- feature/*
- development
- main

## 4.1. feature/**

![feature pipeline](sources/feature-pipline.drawio.svg)

De feature pipeline zal de pipelinezijn die het meeste gaat draaien, als je ziet in [Feature pipeline](https://github.com/delaygram/delay-frontend/issues/6) is te zien welke stappen allemaal uitgevoerd zullen worden tijdens een push event met de branch naam `feature/**`.

De volgende stappen worden dan ook uitgevoerd:
- **Set-up node:** In de set-up node wordt ervoor gezorgd dat de cache opgehaald die momenteel beschikbaar is
- **Install dependencies:** De dependencies die momenteel nog niet bestaan worden geinstalleerd en beschikbaar gesteld
- **Build staging:** In de build staging wordt de applicatie gebouwd met het staging profiel om te kijken of deze slaagt
- **Testing:** Testen worden uitgevoerd en een rapport wordt gegenereerd om te gebruiken in SonarCloud
- **SonarCloud:** De SonarCloud (linting/validatie) wordt uitgevoerd en de code coverage wordt meegenomen van de vorige stap

```yaml
on:
  push:
    branches:
      - "feature/**"

jobs:
  build:
    name: Build and test
    runs-on: ubuntu-20.04

    strategy:
      matrix:
        node-version: [14.x]

    steps:
      - name: Git checkout
        uses: actions/checkout@v2

      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v1
        with:
          node-version: ${{ matrix.node-version }}

      - name: Cache node modules
        id: cache-nodemodules
        uses: actions/cache@v2
        env:
          cache-name: cache-node-modules
        with:
          path: node_modules
          key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
          restore-keys: |
            ${{ runner.os }}-build-${{ env.cache-name }}-
            ${{ runner.os }}-build-
            ${{ runner.os }}-

      - name: Install Dependencies
        if: steps.cache-nodemodules.outputs.cache-hit != 'true'
        run: npm ci

      - name: Install angular CLI
        run: npm i -g @angular/cli

      - name: Build
        run: ng build --configuration staging

      - name: Lint
        run: ng lint

      - name: Test
        run: ng test -- --browsers=ChromeHeadless --watch=false --code-coverage

      - name: SonarCloud Scan
        uses: SonarSource/sonarcloud-github-action@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}
```

> **Source:** [Feature pipeline](https://github.com/delaygram/delay-frontend/blob/main/.github/workflows/front.feature.push.yml)

## 4.2. development

![Development pipeline](/sources/develop-pipeline.drawio.svg)

In de development pipeline is het de bedoeling om dezelfde stappen uit te voeren die ook in de `feature/*` pipeline staan, maar hier worden een aantal extra stappen uitgevoerd, denk hier aan deployment naar de staging `environment`. De stappen die **extra** worden uitgevoerd, staan hieronder uitgelegd:
- **Feature:** Alle stappen van de [feature pipeline](#51-feature)
- **Tag build:** De build wordt op dit moment getagd om te weten waar dit als laatst fout is gegaan, de tag heeft de naam `build-{build number}`
- **Deploy staging:** De applicatie wordt live gezet op de staging environment wat te bereiken is via [https://staging.delaygram.nl/](https://staging.delaygram.nl/)
- **Tag release:** De release krijgt een tag om te zien welke code nu precies op de live staging omgeving staat
- **Publish test results:** Alle test resultaten die in de pipeline zijn gegenereerd worden gepubliceerd naar een S3 bucket in AWS om de resultaten terug te kunnen halen

```yaml
on:
  push:
    branches:
      - "development"

jobs:
  build:
    name: Build and test
    runs-on: ubuntu-20.04

    strategy:
      matrix:
        node-version: [14.x]

    steps:
      - name: Git checkout
        uses: actions/checkout@v2

      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v1
        with:
          node-version: ${{ matrix.node-version }}

      - name: Cache node modules
        id: cache-nodemodules
        uses: actions/cache@v2
        env:
          cache-name: cache-node-modules
        with:
          path: node_modules
          key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
          restore-keys: |
            ${{ runner.os }}-build-${{ env.cache-name }}-
            ${{ runner.os }}-build-
            ${{ runner.os }}-

      - name: Install Dependencies
        if: steps.cache-nodemodules.outputs.cache-hit != 'true'
        run: npm ci

      - name: Install angular CLI
        run: npm i -g @angular/cli

      - name: Build
        run: ng build --configuration staging

      - name: Lint
        run: ng lint

      - name: Test
        run: ng test -- --browsers=ChromeHeadless --watch=false --code-coverage

      - name: SonarCloud Scan
        uses: SonarSource/sonarcloud-github-action@master
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}

      - name: Set up AWS credentials
        uses: aws-actions/configure-aws-credentials@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: ${{ secrets.AWS_REGION }}

      - name: Setup Git
        run: |
          git config --local user.email ${{ secrets.EMAIL }}
          git config --local user.name ${{ github.actor }}

      - name: Tag build
        run: |
          git tag -a build-${{ github.run_number }} -m "Tag for github build-${{ github.run_number }}"
          git push origin build-${{ github.run_number }}

      - name: Deploy to staging bucket
        run: aws s3 sync dist/delay-frontend s3://delaygram-staging/

      - name: Run invalidation on staging CloudFront
        run: aws cloudfront create-invalidation --distribution-id E2VCGQ0ORDECMP --paths "/*"

      - name: Tag release
        run: |
          git tag -a release-${{ github.run_number }} -m "Tag for github release-${{ github.run_number }}"
          git push origin release-${{ github.run_number }}

      - name: Publish test results
        run: |
          aws s3 cp coverage/delay-frontend s3://delaygram-testresults/frontend/build-${{ github.run_number }} --recursive
```
> **Source:** [Development pipeline](https://github.com/delaygram/delay-frontend/blob/main/.github/workflows/front.develop.push.yml)

## 4.3. main
![Main pipeline](/sources/main-pipeline.drawio.svg)

In de main pipeline loopt het net wat anders, hier hoeven namelijk geen tests meer uitgevoerd worden, omdat deze gevalideerd en gecontroleerd zijn in de feature en development pipelines. Daarvoor worden de stappen van de main pipeline hieronder toegelicht:
- **Set-up node:** In het begin van de pipeline wordt node opgezet, de huidige cached versie opgehaald, missende dependencies geinstalleerd
- **Build production:** Nu is het de bedoeling om de production build te bouwen om ook de correcte environments beschikbaar te krijgen
- **Deploy production:** De applicatie wordt live gezet in de productie opgeving die te bereiken is via [https://delaygram.nl/](https://delaygram.nl/)
- **Tag production:** Er wordt een production tag neergezet met de naam `production` om te zien welke commit momenteel op de live omgeving staat

```yaml
on:
  push:
    branches:
      - "main"

jobs:
  build:
    name: Build and test
    runs-on: ubuntu-20.04

    strategy:
      matrix:
        node-version: [14.x]

    steps:
      - name: Git checkout
        uses: actions/checkout@v2

      - name: Use Node.js ${{ matrix.node-version }}
        uses: actions/setup-node@v1
        with:
          node-version: ${{ matrix.node-version }}

      - name: Cache node modules
        id: cache-nodemodules
        uses: actions/cache@v2
        env:
          cache-name: cache-node-modules
        with:
          path: node_modules
          key: ${{ runner.os }}-build-${{ env.cache-name }}-${{ hashFiles('**/package-lock.json') }}
          restore-keys: |
            ${{ runner.os }}-build-${{ env.cache-name }}-
            ${{ runner.os }}-build-
            ${{ runner.os }}-
      - name: Install Dependencies
        if: steps.cache-nodemodules.outputs.cache-hit != 'true'
        run: npm ci

      - name: Install angular CLI
        run: npm i -g @angular/cli

      - name: Build
        run: ng build --configuration production

      - name: Set up AWS credentials
        uses: aws-actions/configure-aws-credentials@v1
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: ${{ secrets.AWS_REGION }}

      - name: Setup Git
        run: |
          git config --local user.email ${{ secrets.EMAIL }}
          git config --local user.name ${{ github.actor }}
      - name: Deploy to production bucket
        run: aws s3 sync dist/delay-frontend s3://delaygram-prod/

      - name: Run invalidation on production CloudFront
        run: aws cloudfront create-invalidation --distribution-id E1UYS7U2IXL3JN --paths "/*"

      - name: Tag production
        run: |
          git tag -a production -m "Tag for github production"
          git push origin production
```
> **Source:** [Main pipeline](https://github.com/delaygram/delay-frontend/blob/main/.github/workflows/front.main.push.yml)

# 5. Conclusie

Nu de pipelines staan en de builds en test worden uitgevoerd bij elke push, is er geen omkijken meer naar het deployen van de applicatie, linting van de applicatie en validatie in SonarCloud. Wat dit uiteindelijk wilt zeggen is dat er veel handmatig werk is komen te vervallen, waardoor er meer tijd over is voor het developen van de applicatie.