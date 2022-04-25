# 1. Contents

- [1. Contents](#1-contents)
- [2. Delaygram software](#2-delaygram-software)
- [3. Document historie](#3-document-historie)
- [4. Aandeelhouders](#4-aandeelhouders)
- [5. Introductie](#5-introductie)
- [6. Project beschrijving](#6-project-beschrijving)
- [7. Projectmanagement tools](#7-projectmanagement-tools)
  - [7.1. Scrum](#71-scrum)
  - [7.2. GitHub Project Board](#72-github-project-board)
  - [7.3. GitHub](#73-github)
- [8. Sprints](#8-sprints)
  - [8.1. Sprint 0](#81-sprint-0)
    - [8.1.1. Goals](#811-goals)
    - [8.1.2. Planning](#812-planning)
    - [8.1.3. Achievements](#813-achievements)
    - [8.1.4. Retrospective](#814-retrospective)
  - [8.2. Sprint 1](#82-sprint-1)
- [9. Requirements](#9-requirements)
  - [9.1. User stories](#91-user-stories)
  - [9.2. Functionele requirements](#92-functionele-requirements)
  - [9.3. Non-functionele requirements](#93-non-functionele-requirements)
- [10. Architektuur Design](#10-architektuur-design)
  - [10.1. Systeem contxt](#101-systeem-contxt)
  - [10.2. Container Diagram](#102-container-diagram)
- [11. DevOps](#11-devops)
  - [11.1. CI/CD tools](#111-cicd-tools)
  - [11.2. Pipeline](#112-pipeline)
    - [11.2.1. feature/**](#1121-feature)
    - [11.2.2. development](#1122-development)
    - [11.2.3. main](#1123-main)
- [12. Referenties](#12-referenties)

# 2. Delaygram software

|              |            |
| ------------ | ---------- |
| Project      | Delaygram  |
| Team         | Rick Meels |
| Versie       | 0.1        |
| Versie datum | 21-2-2022  |
| Status       | Concept    |

# 3. Document historie

| Versie | Veranderingen                                                                                                                                                       | Auteur     | Datum     |
| -----: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------- |
|    0.1 | Eerste opzet document                                                                                                                                               | Rick Meels | 20-2-2022 |
|    0.2 | Invullen van de volgende onderdelen:<br>- Introductie<br>- Project omschrijving<br>- Projectmanagement tools<br>- Non-functionals opzetten<br>- DevOps beschrijving | Rick Meels | 21-2-2022 |
|    0.3 | Invullen van de volgende onderdelen:<br>- Systeem Context<br>- Container Diagram<br>- Updated images with svg's                                                     | Rick Meels | 23-2-2022 |

# 4. Aandeelhouders

| Naam         | Email                     | Bedrijf | Rol               |
| ------------ | ------------------------- | ------- | ----------------- |
| Merel Veracx | m.veracx@fontys.nl        | Fontys  | Technical Contact |
| Frank Coenen | f.coenen@fontys.nl        | Fontys  | Technical Contact |
| Rick Meels   | r.meels@student.fontys.nl | Fontys  | Uitvoerder        |


# 5. Introductie

In dit document wordt het softwarepakket voor Delaygram beschreven.

Delaygram is een softwarepakket voor eindgebruikers die een makkelijke en eenvoudige manier zoeken om foto’s en/of korte video’s te delen met hun vrienden of volgers. Hiermee betrek je je dagelijkse volgers of vrienden in de leuke activiteiten, plaatjes of filmpjes die jij hebt gemaakt.

Het project zal bestaan uit een webapplicatie die te gebruiken is voor gebruikers die plaatjes of filmpjes willen posten op het platform. Een mobiele app is nog een discussie over of deze gerealiseerd zal worden. 
De te gebruiken technieken staan nog van tevoren vast, hier zal tijdens het project voor gekozen worden. Er is ook een mogelijkheid om verschillende technieken door elkaar heen te gebruiken.

Vanuit het ontwikkelteam is er voor de webapplicatie een voorkeur voor Angular maar hier kan vanaf geweken worden wanneer dit voordelen met zich meebrengt.

# 6. Project beschrijving

Het is een systeem waarbij gebruikers foto’s en video’s kunnen delen met hun volgers en/of vrienden om dagelijkse of reis activiteiten te kunnen delen. Zo is het mogelijk om mensen met elkaar verbonden te houden en zo een kijkje mee te geven in de avonturen van een ander.

Daarbij is het mogelijk om gebruikers te volgen en reacties achter te laten op de post van een ander, zo blijft er activiteit op het platform om mensen verbonden te houden. Daarnaast zijn er mogelijkheden zoals het liken van post waarbij de persoon die het heeft geplaatst een bericht van krijgt. 

# 7. Projectmanagement tools

## 7.1. Scrum

Om het project in goede banen te leiden is er gekozen om de scrum methode te gebruiken. Er is voor Scrum gekozen omdat er binnen het ontwikkelteam een goede ervaring mee is. Ook kan hierdoor de voortgang goed bij worden gehouden en problemen optijd gesignaleerd worden. Hierbij zal worden gewerkt in sprints van 3 weken waarbij minimaal 2 werkdagen per week besteed zal worden aan dit project. 

## 7.2. GitHub Project Board

Er is voor GitHub project board gekozen omdat het een goede manier is om de projecten te organiseren. Hier kan je de verschillende onderdelen van het project aan elkaar koppelen. Hierdoor kan je de verschillende onderdelen van het project in een goede volgorde laten zien.

Er is gekozen voor een GitHub project board ten opzichte van een ander project management systeem, omdat de integratie met GitHub zelf veel makkelijker is.

GitHub project board is gratis te gebruiken.

## 7.3. GitHub

Het versiebeheer van code wordt gedaan door middel van Git, Hier heeft het ontwikkelteam veel ervaring mee. De code wordt opgeslagen op GitHub, deze keuze is gemaakt omdat het mogelijk is om een GitHub Organisation aan te maken. Hierdoor staan de repositories voor de verschillende componenten op een overzichtelijke manier gegroepeerd. Er zijn verschillende opties hiervoor bekeken maar deze waren of niet gratis te gebruiken of hadden geen optie voor het maken van organisaties of groepen voor repositories.

Omdat er gebruik gemaakt wordt van de gratis optie is alle code open source, dit is geen probleem omdat dit een leerproject is.

Hieronder staat de url voor de GitHub Organisation, hierin staan alle repositories voor dit project. <https://github.com/orgs/delaygram>

# 8. Sprints

In dit hoofdstuk worden doelen en resultaten van de verschillende sprints toegelicht. Dit zal voor een groot deel gaan aan de hand van screenshots van het Scrum bord die op de Github project board staan.

## 8.1. Sprint 0

### 8.1.1. Goals

Deze sprint zal toegewijd zijn aan het opzetten van het project. De eisen voor het product zullen vastgelegd worden. Ook zal er veel tijd besteed worden aan het kiezen van de juiste tooling voor het project zoals versiebeheer, storyboard, pipeline toosl en deployment omgevingen. Er zal ook een eerste opzet voor een architectuur worden gemaakt.

### 8.1.2. Planning

![Project board sprint 0](/img/project-board-sprint-0.png)

### 8.1.3. Achievements

De opdrachtomschrijving is gemaakt, ook is alle tooling die nodig is om het project te starten opgezet. Verder zijn er nog uitgebreidere beschrijvingen gemaakt mbt de opdracht en project omschrijving. Verder is de planning opgezet voor de eerste sprint (sprint 0) om uiteindelijk een goede start te kunnen maken aan de komende sprints. Daarnaast is er nog een [Project pitch](sources/project-pitch.pptx) gemaakt om een duidelijk beeld te geven aan de docenten wat precies de bedoeling is.

### 8.1.4. Retrospective

## 8.2. Sprint 1

# 9. Requirements

## 9.1. User stories

## 9.2. Functionele requirements

Hieronder staat de lijst van de functionele requirements van het software pakket. Ze hebben allemaal een prioriteit gekregen waarmee rekening wordt gehouden in de ontwikkelingsvolgorde, requirements met een hogere prioriteit zullen wanneer mogelijk eerder geïmplementeerd worden.

|     | Omschrijving                             | Prioriteit |
| --- | ---------------------------------------- | ---------- |
| F1  | Een gebruiker moet zich kunnen aanmelden | M          |

## 9.3. Non-functionele requirements

In dit hoofdstuk zullen de non-functionele requirements van het product worden beschreven.

|     | Categorie           | Beschrijving                                                                                                                                                    |
| --- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| N1  | Security            | De applicatie moet veilig zijn. Alle verzoeken van en naar services zullen door middel van TLS beveiligd worden.                                                |
| N2  | Privacy             | De gegevens van gebruikers moet veilig opgeslagen worden. Ook zullen er geen gegevens die niet nodig zijn voor de bedrijfsvoering worden opgeslagen.            |
| N3  | Reliability         | De tijd tussen het falen van de applicatie zal zo lang mogelijk zijn.                                                                                           |
| N4  | Testability         | De software wordt getest op verschillende niveau's, dit zal ook voor elke release van de software gedaan worden.                                                |
| N5  | Data integrity      | De data wordt op een veilige manier opgeslagen en zal voldoen aan de GDPR.                                                                                      |
| N6  | Documentation       | Allen onderdelen zullen uitgebreid gedocumenteerd worden.                                                                                                       |
| N7  | Extensibility       | Het platform zal op een manier worden gebouwd dat deze goed uit te breiden is                                                                                   |
| N8  | Open source         | Alle code zal als open source op GitHub staan.                                                                                                                  |
| N9  | Performance         | Alle verzoeken binnen de applicatie (met uitzondering van de zware bereken functies) zullen over een goeie wifiverbinding binnen 2 seconden een reactie sturen. |
| N10 | Quality             | De kwaliteit van de code zal hoog zijn, deze wordt bewaakt door middel van de tooling die hiervoor beschikbaar is.                                              |
| N11 | Scalability         | Het platform zal op een manier worden gebouwd dat deze op een eenvoudige manier op te schalen is wanneer hier vraag voor is.                                    |
| N12 | Compatibility       | Het platform zal op alle moderne besturingssystemen beschikbaar en functioneel zijn.                                                                            |
| N13 | Highly availability | Het platform zal op een highly availability structuur gebouwd worden waardoor de downtime zo klein mogelijk is.                                                 |
| N14 | Monitoring          | Het platform zal op een centrale plek gemonitord worden.                                                                                                        |

**BEWIJSLASTEN NON-FUNCTIONALS**

# 10. Architektuur Design

## 10.1. Systeem contxt
 
![Systeem Context](/img/systeem-context.svg)

Hierboven is de systeem context te zien. Hier staan de verbindingen met externe applicaties en hoe deze met elkaar communiceren. Ook zijn de verschillende rollen te zien en hoe deze het systeem gebruiken.

## 10.2. Container Diagram

![Container diagram](/img/container-diagram.svg)

Hierboven staat een diagram waar de architectuur iets duidelijker in beeld is gebracht. Zo valt te zien dat er een frontend service die met de backend praat. De backend services zullen praten met verschillende datastores. Ook staat de verbinding met Cognito en SNS services ertussen.

![Service Datastore](/img/service-datastore.svg)

Elke service is opgezet met een Datastore eracher, deze bestaat in alle gevallen uit een NoSQL database. In de volgende afbeelding zullen de datastores en services als een object gepresenteerd worden.



# 11. DevOps

## 11.1. CI/CD tools

Uit onderzoek dat gedaan is bij [#6](https://github.com/delaygram/portfolio/issues/6) is gebleken dat GitHub actions de meeste geschikte tool is. Hier zijn veel mouwminuten beschikbaar.

## 11.2. Pipeline

### 11.2.1. feature/**

![feature pipeline](/sources/feature-pipline.drawio.svg)

De feature pipeline zal de pipelinezijn die het meeste gaat draaien, als je ziet in [Feature pipeline](https://github.com/delaygram/delay-frontend/issues/6) is te zien welke stappen allemaal uitgevoerd zullen worden tijdens een push event met de branch naam `feature/**`.

De volgende stappen worden dan ook uitgevoerd:
- **Set-up node:** In de set-up node wordt ervoor gezorgd dat de cache opgehaald die momenteel beschikbaar is
- **Install dependencies:** De dependencies die momenteel nog niet bestaan worden geinstalleerd en beschikbaar gesteld
- **Build staging:** In de build staging wordt de applicatie gebouwd met het staging profiel om te kijken of deze slaagt
- **Testing:** Testen worden uitgevoerd en een rapport wordt gegenereerd om te gebruiken in SonarCloud
- **SonarCloud:** De SonarCloud (linting/validatie) wordt uitgevoerd en de code coverage wordt meegenomen van de vorige stap

<details>
  <summary>Feature pipeline</summary>
  
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
</details>

### 11.2.2. development

![Development pipeline](/sources/develop-pipeline.drawio.svg)

In de development pipeline is het de bedoeling om dezelfde stappen uit te voeren die ook in de `feature/*` pipeline staan, maar hier worden een aantal extra stappen uitgevoerd, denk hier aan deployment naar de staging `environment`. De stappen die **extra** worden uitgevoerd, staan hieronder uitgelegd:
- **Feature:** Alle stappen van de [feature pipeline](#51-feature)
- **Tag build:** De build wordt op dit moment getagd om te weten waar dit als laatst fout is gegaan, de tag heeft de naam `build-{build number}`
- **Deploy staging:** De applicatie wordt live gezet op de staging environment wat te bereiken is via [https://staging.delaygram.nl/](https://staging.delaygram.nl/)
- **Tag release:** De release krijgt een tag om te zien welke code nu precies op de live staging omgeving staat
- **Publish test results:** Alle test resultaten die in de pipeline zijn gegenereerd worden gepubliceerd naar een S3 bucket in AWS om de resultaten terug te kunnen halen

<details>
  <summary>Development pipeline</summary>

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
</details>




### 11.2.3. main

![Main pipeline](/sources/main-pipeline.drawio.svg)

In de main pipeline loopt het net wat anders, hier hoeven namelijk geen tests meer uitgevoerd worden, omdat deze gevalideerd en gecontroleerd zijn in de feature en development pipelines. Daarvoor worden de stappen van de main pipeline hieronder toegelicht:
- **Set-up node:** In het begin van de pipeline wordt node opgezet, de huidige cached versie opgehaald, missende dependencies geinstalleerd
- **Build production:** Nu is het de bedoeling om de production build te bouwen om ook de correcte environments beschikbaar te krijgen
- **Deploy production:** De applicatie wordt live gezet in de productie opgeving die te bereiken is via [https://delaygram.nl/](https://delaygram.nl/)
- **Tag production:** Er wordt een production tag neergezet met de naam `production` om te zien welke commit momenteel op de live omgeving staat

<details>
  <summary>Main pipeline</summary>

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

</details>

# 12. Referenties
