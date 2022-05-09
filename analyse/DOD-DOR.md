# 1. Inhoud

- [1. Inhoud](#1-inhoud)
- [2. Document historie](#2-document-historie)
- [3. Introductie](#3-introductie)
- [4. Algemene definitions](#4-algemene-definitions)
  - [4.1. Definition of Ready](#41-definition-of-ready)
  - [4.2. Definition of Done](#42-definition-of-done)
    - [4.2.1. Code Standaard](#421-code-standaard)
    - [4.2.2. Documentatie](#422-documentatie)
    - [4.2.3. Quality](#423-quality)
    - [4.2.4. Monitoring](#424-monitoring)
    - [4.2.5. Performance](#425-performance)
- [5. User stories en specifieke onderdelen DoR & DoD](#5-user-stories-en-specifieke-onderdelen-dor--dod)
  - [Gebruikers registratie](#gebruikers-registratie)
    - [User Story](#user-story)
    - [Definition of Ready](#definition-of-ready)
    - [Definition of Done](#definition-of-done)
  - [Gebruikers validatie](#gebruikers-validatie)
    - [User Story](#user-story-1)
    - [Definition of Ready](#definition-of-ready-1)
    - [Definition of Done](#definition-of-done-1)
  - [Gebruikers inloggen](#gebruikers-inloggen)
    - [User Story](#user-story-2)
    - [Definition of Ready](#definition-of-ready-2)
    - [Definition of Done](#definition-of-done-2)

# 2. Document historie

| Versie | Veranderingen                                                                                  | Datum      |
| -----: | ---------------------------------------------------------------------------------------------- | ---------- |
|    0.1 | Eerste opzet document                                                                          | 19-04-2022 |

# 3. Introductie

In dit document wordt toegelicht wat de DoD (Definition of Done) en DoR (Definition of Ready) is voor de betreffende user stories. De user stories hebben allemaal hun eigen DoD en DoR, met bovenin een aantal algemene DoD en DoR die gelden voor alle user stories.

# 4. Algemene definitions

## 4.1. Definition of Ready

- User Story opgenomen in dit document
- Afhankelijkheid van andere functionaliteit in kaart gebracht
- Functionele requirements beschreven in DoD bij User Story

## 4.2. Definition of Done

### 4.2.1. Code Standaard

- Consistente en leesbare code
- Alle benodigde aws-resources vastgelegd in sam/cloudformation-template

### 4.2.2. Documentatie

- Publieke api's zijn gedocumenteerd

### 4.2.3. Quality

- Unit test(en) geschreven. Zinnige tests zijn belangrijker dan percentage coverage, maar er wordt naar volledige dekking gestreefd dus er wordt minstens een percentage boven de 80% verwacht
- Functional test(en) geschreven voor endpoints van publieke api's
- Test coverage is meegenomen in de SonarCloud scan
- SonarCloud analyse bekeken, punten zijn opgelost of kunnen als onschadelijk worden beschouwd
- QualityGate passed
- Deployment naar production

### 4.2.4. Monitoring

- Logging toegepast
- X-Ray toegepast
- Per Bounded-Context een CloudWatch-DashBoard met de belangrijkste metrics

### 4.2.5. Performance

- Performance tests geschreven voor verwachtte hotpaths

# 5. User stories en specifieke onderdelen DoR & DoD

## Gebruikers registratie

### User Story

Als een uitgelogde gebruiker wil ik een nieuw account willen registreren zodat ik mijn nieuw aangemaakte account kan verifiëren.

### Definition of Ready

- Er is bepaald welke attributen verplicht zijn voor een user om zich te kunnen registeren
- Er is bepaald welk attribuut gebruikt gaat worden om mee in te loggen

### Definition of Done

- Gebruiker moet de mogelijkheid hebben om een nieuw account te kunnen registreren met email, gebruikersnaam en wachtwoord
- Gebruiker moet een bericht krijgen als de gekozen gebruikersnaam al in gebruik is
- Gebruiker moet een email krijgen na de registratie voor het activeren van het account

## Gebruikers validatie

### User Story

Als een uitgelogde gebruiker wil ik mijn account kunnen activeren zodat ik kan inloggen op mijn nieuw aangemaakte account.

### Definition of Ready

- Er is bepaald welke attributen verplicht zijn voor een user om zich te kunnen verifiëren

### Definition of Done

- Een gebruiker zal zijn account moeten verifiëren, voordat hij/zij kan inloggen
- De gebruiker zal bericht krijgen als de ingevoerde code niet correct is

## Gebruikers inloggen

### User Story

Als een uitgelogde gebruiker wil ik kunnen inloggen op mijn account, zodat ik bij mijn persoonlijke informatie kan komen

### Definition of Ready

- Er is bepaald welke attributen verplicht zijn voor een user om zich te kunnen inloggen

### Definition of Done

- Gebruiker moet zich kunnen inloggen met een correct ingevoerde gebruikersnaam en wachtwoord
- Gebruiker krijgt een bericht als de gebruikersnaam en/of wachtwoord incorrect is ingevuld

