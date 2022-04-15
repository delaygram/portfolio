# 1. Contents

- [1. Contents](#1-contents)
- [2. Document historie](#2-document-historie)
- [3. Begrippenlijst](#3-begrippenlijst)
- [4. Projectopdracht](#4-projectopdracht)
  - [4.1. Probleemstelling](#41-probleemstelling)
  - [4.2. Doel van het project](#42-doel-van-het-project)
  - [4.3. Begrenzing en Randvoorwarden](#43-begrenzing-en-randvoorwarden)
  - [4.4. Strategie](#44-strategie)
  - [4.5. Succesfactoren](#45-succesfactoren)
  - [4.6. Belangrijke data](#46-belangrijke-data)
  - [4.7. Onderzoeksplan](#47-onderzoeksplan)
  - [4.8. Onderzoek](#48-onderzoek)
    - [4.8.1. Onderzoeksvragen](#481-onderzoeksvragen)
      - [4.8.1.1. Hoofdvraag](#4811-hoofdvraag)
      - [4.8.1.2. Deelvragen](#4812-deelvragen)
    - [4.8.2. Onderzoeksmethodes](#482-onderzoeksmethodes)
    - [4.8.3. Scope](#483-scope)
  - [4.9. Eindproducten](#49-eindproducten)
- [5. Activiteiten en tijdsplan](#5-activiteiten-en-tijdsplan)
  - [5.1. Opdeling en aanpak van het project](#51-opdeling-en-aanpak-van-het-project)
  - [5.2. Overall tijdsplan](#52-overall-tijdsplan)
- [6. Testaanpak en Configuratiemanagement](#6-testaanpak-en-configuratiemanagement)
  - [6.1. Testaanpak/strategie](#61-testaanpakstrategie)
  - [6.2. Lijst technieken](#62-lijst-technieken)
  - [6.3. Configuratiemanagement](#63-configuratiemanagement)
- [7. Referenties](#7-referenties)

# 2. Document historie

| Versie | Veranderingen                        | Auteur     | Datum      |
| -----: | ------------------------------------ | ---------- | ---------- |
|    0.1 | Eerste opzet document                | Rick Meels | 07-03-2022 |
|    0.3 | Invullen onderdelen 3 t/m 4.7        | Rick Meels | 09-03-2022 |
|    0.2 | Invullen alle onderdelen 4.8 t/m 6.3 | Rick Meels | 13-03-2022 |

# 3. Begrippenlijst

| Begrip   | Omschrijving                                                                                                                                                                                                                                           |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Big Data | Big data of massadata zijn gegevensverzamelingen (datasets) die te groot en te weinig gestructureerd zijn om met reguliere databasemanagementsystemen te worden onderhouden.<sup>[1](#7-referenties)</sup>                                               |
| DevOps   | DevOps, een combinatie van ontwikkeling (Dev) en bedrijfsactiviteiten (Ops), is de samenstelling van mensen, processen en technologie om doorlopend waarde aan klanten te bieden.<sup>[2](#7-referenties)</sup>                                          |
| CI/CD    | Continuous Integration (CI) en Continuous Delivery (CD) is de benaming voor een manier van werken binnen software teams, waarbij de afhandeling van codewijzigingen wordt gedaan door een aantal geautomatiseerde stappen.<sup>[3](#7-referenties)</sup> |

# 4. Projectopdracht

## 4.1. Probleemstelling

Momenteel zijn er veel mensen die hun foto's en/of video's kwijt willen, maar het liever niet willen plaatsen op de servers van een van de grote corperaties (ex. Facebook, Instagram, Twitter, etc.). Dit heeft te maken dat grote corperaties gebruik maken van de geplaatste content en zo een profiel van jou kunnen maken en gerichter kunnen adverteren.

Daarom moet er een oplossing komen waar grote corperaties niet bij kunnen en dus geen [Big Data](#3-begrippenlijst) verzamelen. Om dat probleem te verhelpen moet er een nieuw onafhankelijk product worden gebouwd. Dit product moet een webapplicatie zijn die gebruikers kunnen gebruiken om content te plaatsen om zo te delen met andere gebruikers.

## 4.2. Doel van het project

Om dit probleem te verhelpen moet er een nieuw onafhankelijk product worden gebouwd. Dit product gaat de naam [Delaygram](https://delaygram.nl/) krijgen. 

[Delaygram](https://delaygram.nl/) is een softwarepakket voor eindgebruikers die een makkelijke en eenvoudige manier zoeken om foto’s en/of korte video’s te delen met hun vrienden of volgers. Hiermee betrek je je dagelijkse volgers of vrienden in de leuke activiteiten, plaatjes of filmpjes die jij hebt gemaaktof gedaan.

Het project zal bestaan uit een webapplicatie die te gebruiken is voor gebruikers die plaatjes of filmpjes willen posten op het platform. Een mobiele app is nog een discussie over of deze gerealiseerd zal worden. 
De te gebruiken technieken staan nog niet van tevoren vast, hier zal tijdens het project voor gekozen worden. Er is ook een mogelijkheid om verschillende technieken door elkaar heen te gebruiken.

## 4.3. Begrenzing en Randvoorwarden

| Tot het project behoort:                                    | Tot het project behoort niet: |
| ----------------------------------------------------------- | ----------------------------- |
| 1. Analyse en onderzoek                                     | 1.                            |
| 2. Ontwerp en ontwikkeling                                  |                               |
| 3. Implementatie                                            |                               |
| 4. Testen                                                   |                               |
| 5. Planning                                                 |                               |
| 6. [DevOps](#3-begrippenlijst) ([CI/CD](#3-begrippenlijst)) |                               |

## 4.4. Strategie

Het project is in grote lijnen volgens het waterval principe. De keuze voor een waterval methodiek is gemaakt op basis van de scope van het project. Het project zal een vaststaande scope hebben voor de gehele ontwikkelfase en zullen tijdens het verloop van het project niet of nauwelijks aangepast worden.

- **Probleemdefinitiefase**
  - In deze fase wordt er onderzoek gedaan naar de inhoud van de gegeven opdracht. Op basis van het onderzoek kan er een verwachting geschetst worden voor de op te leveren product(en).

- **Analysefase**
  - In deze fase zal er gewerkt worden aan het Requirements Analyse Document (RAD) om een basis te vormen voor een goed projectresultaat en zullen er onderzoeken worden opgesteld. Deze onderzoeken zullen tijdens de loop van het project duidelijkheid moeten schetsen en de uiteindelijke onderzoeksvragen beantwoorden.
- **Designfase**
  - In deze fase zal er een Software Architectuur Document (SAD) en een Systeemtestplan gemaakt worden. Met een SAD wordt een duidelijk beeld creëren hoe de applicatie op de achtergrond eruit gaat zien, daarnaast zal het testplan gemaakt worden om een duidelijk beeld te krijgen hoe en waar in de applicatie getest zal worden. Verder zal er een begin worden gemaakt aan de applicatie zelf.
- **Implementatiefase**
  - Deze fase zal grotendeels de focus liggen op het maken en implementeren van de al hiervoor beschreven software architectuur. Tijdens de implementatie zal de applicatie grondig getest worden op basis van unittests, code analysis en code reviews.
- **Afrondingsfase**
  - In deze fase zullen de laatste wijzigingen en puntjes op de “i” worden gezet, denk hierbij aan bug fixes, laatste features, documentatie, portfolio en dergelijke. 

## 4.5. Succesfactoren

Om het project succesvol te laten slagen moet er voldaan worden aan alle acceptatiecriteria van de individuele user stories. Naast deze acceptatiecriteria zijn er nog een aantal andere factoren die bepalen of het project succesvol is of niet:

- Zorg dat gebruikers makkelijk content kunnen uploaden doormiddel van een uploadservice.
- Maak het overbodig voor gebruikers om eindeloos te zoeken op de webapplicatie.
- Maak het product responsive om ervoor te zorgen dat verzoeken niet te lang duren.

## 4.6. Belangrijke data

Naast alle planningen zijn er belangrijke data die eventueel invloed kunnen hebben op het project.

| Datum      | Gebeurtenis                                                                                                |
| ---------- | ---------------------------------------------------------------------------------------------------------- |
| 20-02-2022 | [Project Pitch](https://fhict.instructure.com/courses/12090/modules/items/751927)                          |
| 13-03-2022 | [Emerging Trends Research: Plan](https://fhict.instructure.com/courses/12090/modules/items/751924)         |
| 20-03-2022 | [Sprint 1](https://fhict.instructure.com/courses/12090/modules/items/751928)                               |
| 10-04-2022 | [Sprint 2](https://fhict.instructure.com/courses/12090/modules/items/751929)                               |
| 01-05-2022 | [Sprint 3](https://fhict.instructure.com/courses/12090/modules/items/751930)                               |
| 29-05-2022 | [Sprint 4](https://fhict.instructure.com/courses/12090/modules/items/751931)                               |
| 12-06-2022 | [Emerging Trends Research: Deliverables](https://fhict.instructure.com/courses/12090/modules/items/751925) |
| 19-06-2022 | [Sprint 5](https://fhict.instructure.com/courses/12090/modules/items/751932)                               |
| 19-06-2022 | [Final delivery of documents and code](https://fhict.instructure.com/courses/12090/modules/items/751933)   |

```mermaid
gantt
    title Planning
    dateFormat  DD-MM-YYYY
    section Sprint 1
    Sprint 1           :21-02-2022, 20-03-2022
    section Sprint 2
    Sprint 2           :20-03-2022, 10-04-2022
    section Sprint 3
    Sprint 3           :10-04-2022, 01-05-2022
    section Sprint 4
    Sprint 4           :01-05-2022, 29-05-2022
    section Sprint 5
    Sprint 5           :29-05-2022, 19-06-2022
```

## 4.7. Onderzoeksplan

Alle ioaj zullen uitgevoerd worden met de Methode Toolkit HBO-i. Dit framework biedt gebruikers de mogelijkheid geschikte onderzoeksmethoden te selecteren, geeft aanwijzingen voor het gebruik en wijst naar geschikte bronnen om meer diepgang te geven.

Voor een beschrijving van de onderzoeksmethodes, vindt hier onder een korte beschrijving van de verschillende methodes.

| Image                                      | Beschrijving                                                                                                                                                                                                                                                      |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ![Library](/img/projectplan/library.png)   | De library onderzoeksstrategie wordt gebruikt al om al bestaande theorieën en richtlijnen te verkennen. Die verder kunnen helpen het onderzoek te ondersteunen.                                                                                                   |
| ![Field](img/projectplan/field.png)        | De field onderzoeksstrategie wordt gebruikt om de applicatie context te verkennen. Deze strategie wordt gebruikt om de behoeftes, verlangens en beperkingen van de eindgebruikers te leren kennen.                                                                |
| ![Lab](img/projectplan/lab.png)            | De lab onderzoeksstrategie wordt gebruikt om onderdelen of concepten van het product te testen. Deze strategie wordt gebruikt om erachter te komen of onderdelen werken zoals ze bedacht zijn of om verschillende scenario’s te testen.                           |
| ![Showroom](/img/projectplan/showroom.png) | De showroom onderzoeksstrategie wordt gebruikt om ideeën in relatie met al bestaand werk te testen. Het tonen van een prototype aan experts kan een vorm van showroom onderzoek zijn of het pitchen waarom een project anders is dan de rest van de concurrentie. |
| ![Workshop](/img/projectplan/workshop.png) | De workshop onderzoeksstrategie wordt gebruikt om kansen te verkennen. Prototyping, designen en co-creatie zijn manieren om inzicht te krijgen in wat mogelijk is en hoe bepaalde dingen kunnen functioneren.                                                     |

## 4.8. Onderzoek

In de opdracht komen veel technieken en werkwijzen aan bod. De opdracht werkt meerdere deelvragen uit. Een groot deel van de strategieën van het onderzoeks framework zijn toepasbaar tijdens dit project.

### 4.8.1. Onderzoeksvragen

#### 4.8.1.1. Hoofdvraag

Hoe kan [Delaygram](https://delaygram.nl/) functioneren als een integraal geheel, gebaseerd op een enterprice architectuur in de cloud?

#### 4.8.1.2. Deelvragen

1. Hoe wordt de webapplicatie beschikbaar gesteld aan de eindgebruiker in de cloud?
   - Welke services zijn nodig om de applicatie beschikbaar te kunnen stellen in de cloud?
2. Wat is de cloud?
   - Wat is serverless?
   - Wat zijn lambdas?
   - Wat is een API gateway?
3. Hoe wordt een applicatie beschikbaar gesteld via Kubernetes?
   - Wat is k8s?
   - Hoe applicaties te schalen?
4. Hoe wordt er verzekerd dat de applicatie schaalbaar is?
   - Wat betekend schalen van een applicatie?
   - Waarom is schalen van een applicatie zo belangrijk? 

### 4.8.2. Onderzoeksmethodes

|Methode|Uitleg|
|------|------|
|![Library](/img/projectplan/library.png)|**Available product analysis**<br>Door te onderzoeken welke bestaande systemen/oplossingen al op de markt zijn, krijg je een goed beeld van welke oplossingen er al bestaan die goed passen bij dit huidige project en of die een goede aanvulling kunnen zijn.<br><br>**Literature Study**<br>Door bestaande bronnen te onderzoeken die verschillende oplossingen beschrijven, kun je eerder gevonden resultaten gebruiken tot een conclusdie te komen voor dit onderzoek.|
|![Field](img/projectplan/field.png)|**Document Analysis**<br>Documenten bestureen van de betreffende providers en/of producten kunnen gebruikt worden om een goed beeld te krijgen of de gewenste oplossing toe te passen valt op dit project.|
|![Workshop](/img/projectplan/workshop.png)|**Prototyping**<br>Vanzelfsprekend is de beste manier om onderdelen visueel en functioneel te krijgen is door een prototype te maken en de resultaten hiervan te noteren. Zo kan een goed beeld komen op de principes van dit onderzoek.|

### 4.8.3. Scope

De scope van het onderzoek is om te onderzoeken hoe de betreffende applicatie kan worden gebruikt in de cloud en hoe dit op een enterprise architectuur gebaseerd kan worden. De bedoeling is namelijk om de applicatie schaalbaar te maken en onderliggend ervoor zorgen dat de applicatie kan worden gebruikt door meerdere gebruikers tegelijkertijd.

## 4.9. Eindproducten

Hieronder bevindt zich een kort overzicht over de producten die tijdens de stage opgeleverd zullen worden. Daarnaast staat een korte beschrijving over hoe de specifieke onderdelen gerealiseerd zullen worden.

![Product Breakdown Structure](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/delaygram/portfolio/sprint1/img/projectplan/product-breakdown-structure.iuml)

- **Projectplan**
  - Dit document. Het projectplan beschrijft hoe het project zal verlopen.

- **Portfolio**
  - Het portfolio bevat alle documenten en software die tijdens de verloop van het project gemaakt zijn en omschrijft het gehele proces. Denk hierbij aan de analyse, ontwerp, realisatie en test fases waarbij er constant gereflecteerd wordt op de uitvoering.

- **Analysedocument**
  - Onderdeel van de analysefase is een analysedocument. Hier wordt gekeken naar de eisen, wensen en succesfactoren van het project.

- **Architectuurdocument**
  - Tijdens de ontwerpfase wordt het architectuurdocument opgesteld om een goed beeld te krijgen van hoe de software en onderlinge communicatie er technisch uit gaat zien.

- **Testplan**
  - Voor de testfase wordt er een testplan opgesteld waarin tests beschreven staan die de software moet ondergaan. Deze tests zijn zowel functioneel als niet-functioneel. Het testrapport wordt aan de hand van tests ingevuld waarna bepaald wordt of het project succesvol is geweest.

- **Onderzoeksresultaten**
  - Een groot deel van het project is het doen van onderzoek. In dit document worden alle uitgevoerde onderzoeken toegelicht met resultaten en reflecties.

- **Eindapplicatie**
  - Een eindprocut van de delaygram applicatie.

# 5. Activiteiten en tijdsplan

## 5.1. Opdeling en aanpak van het project

De aanpak van het project zal in grote lijnen volgens de vaterval methode verlopen.

1. Opzetten van de requirements (Analyse)
2. Designfase (Architectuur)
3. Bouwen/implementeren van het project (Software)
4. Testfase (Testrapport)
5. Portfolio

## 5.2. Overall tijdsplan

| Fasering      | Effort | Start | Gereed |
| ------------- | :----: | ----- | ------ |
| Opstart       |   5    |       |        |
| Onderzoek     |   30   |       |        |
| Analyse       |   5    |       |        |
| Design        |   10   |       |        |
| Implementatie |   50   |       |        |
| Test          |   20   |       |        |
| Afronding     |   5    |       |        |

Data zijn gebaseerd op ruwe inschattingen en kunnen veranderen. Overpalling van activiteiten kan voorkomen.

# 6. Testaanpak en Configuratiemanagement

## 6.1. Testaanpak/strategie

Om ervoor te zorgen dat dit project en de onderliggende applicaties soepel en goed werken is het nodig om een testaanpak/strategie toe te passen. Daarbij worden de volgende onderdelen in meegenomen:

- **Unit tests**
  - Voor de unit test wordt voornamelijk gebruik gemaakt van JUnit5 (Springboot) en PyTest (Python). JUnit5 is het standaard testing platform voor Java (Springboot) applicaties, net zoals PyTest is dit het standaard testing platform voor Python. Er worden ook vershillende mocking frameworks gebruikt, denk hierbij aan mockito (Springboot) en boto3, pytest-mock, moto (Python). Dit om de testen zo zelf contained als mogelijk te houden.
- **Integration tests**
  - Met integratie testen wordt gebruik gemaakt van @SpringBootTest, TestRestTemplate, MockServer en Gatling (Springboot) en Behave (Python). Dit om de integratie testen te testen op basis van de gemaakte API-endpoints.
- **Performance tests**
  - Om performance tests uit te voeren wordt gebruik gemaakt van Scala hiermee kan op een makkelijke manier de performance van de applicatie worden gemeten in de Sprinboot applicatie en de Python applicatie.
- **Handmatige tests**
  - Als laatste en misschien wel een van de belangrijkere is het handmatig testen van nieuwe componenten en of features die geïmplementeerd zijn. Met handmatig testen worden snel fouten achterhaald die gemaakt zijn tijdens het developen.

## 6.2. Lijst technieken

Om een duidelijk beeld te krijgen wat voor een technieken er precies gebruikt wordt, is hieronder een lijst samengesteld om een makkelijk overzicht te krijgen:

- **Language**
  - Java (Springboot)
  - Python
- **Testing**
  - JUnit5
  - Mockito
  - TestRestTemplate
  - Boto3
  - PyTest-mock
  - Moto
  - Cucumber
- **Coverage & Reports**
  - Coverage (Python)
  - JaCoCo
  - SonarCloud
- **Environments**
  - K8s
  - AWS
  - Docker
  - GitHub Actions

## 6.3. Configuratiemanagement

De gemaakte applicaties worden beheerd via git, GitHub als service. Daarbij wordt gehouden aan de standaard flow.

![GitFlow](/img/projectplan/gitflow.svg)

Elke pull request wordt doormiddel van GitHub Actions gebuild en getest. Na het bouwen en het testen van de applicatie gaat SonarCloud er overheen om te kijken of de code kwaliteit gewaarborgd wordt. Denk hier aan code smells, security hotspots, bugs en vulnerabillities. Na het slagen van alle stappen zullen de aanpassingen gereviewd worden en het vervolgens doorzetten naar development.

Zodra dit naar main gepushed wordt, zal de applicatie in een staging environment komen om de applicatie online te kunnen testen. Indien dit naar behoren werkt kan er een release gemaakt worden en uiteindelijk naar production deployed worden.

# 7. Referenties

1. Wikipedia contributors. (2022, February 25). Big data. *In Wikipedia, The Free Encyclopedia.* Retrieved 10:23, March 7, 2022, from https://en.wikipedia.org/w/index.php?title=Big_data&oldid=1073925279
2. DevOps. *Microsoft Azure.* Retrieved 11:44, March 7, 2022, from https://azure.microsoft.com/nl-nl/overview/what-is-devops/
3. ElasticWeb. (2020, November 27). CI/CD. *Elastic Web.* Retrieved 11:48, March 7, 2022, https://www.elasticweb.nl/kennisbank/continuous-integration-en-continuous-delivery-verder-uitgelegd
