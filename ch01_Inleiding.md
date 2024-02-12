# Inleiding

## Leeswijzer

Dit document beschrijft hoe Logius, afdeling Standaarden (hierna: Logius) de API Standaarden beheert en hoe de bijbehorende governance is ingericht.

### Bijlagen
Practische aspecten van het beheer, zoals de gebruikte applicaties
en webservices zijn opgenomen in bijlagen van dit document.
De bijlagen zijn niet specifiek voor een standaard maar zijn relevant
voor alle standaarden onder beheer bij Logius.

## De API Standaarden

Het begrip API Standaarden is een verzameling van meerdere standaarden. We verstaan hieronder op dit moment de volgende standaarden:

- NLGov REST API Design Rules (In dit document wordt verder ADR gebruikt als afkorting).
- NLGov API Strategie modules (In dit document wordt verder Modules gebruikt als afkorting).
- NLGov Assurance profile for OAuth 2.0 (In dit document wordt verder OAuth-NL gebruikt als afkorting).
- OpenID NLGov (In dit document wordt verder OIDC-NL gebruikt als afkorting).
- NLGov profile for CloudEvents (In dit document wordt verder CloudEvents gebruikt als afkorting).

De API standaarden omvatten een sets van normatieve afspraken voor het structureren, beveiligen, autoriseren, identificeren en documenteren.
De standaarden hebben tot doel om betere, uniforme en ontwikkelaar vriendelijke API’s te ontwikkelen die
makkelijk te implementeren zijn. De sets van afspraken bestaan uit breed toepasbare en ondubbelzinnige richtlijnen.
Deze helpen organisaties die nieuwe API’s ontwikkelen voor Nederlandse overheden (Rijk, provincies, gemeenten en waterschappen) en instellingen uit de (semi-) publieke sector. In ondertsaande tabel zijn alle actuele links opgenomen naar alle bronnen van de standaarden:

| Formele standaard                                            | Gepubliceerde versie                                         | Werk versie                                                  | Repository                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [NLGov API Design Rules (ADR)](https://forumstandaardisatie.nl/open-standaarden/rest-api-design-rules) | [ADR v1 (definitief)](https://gitdocumentatie.logius.nl/publicatie/api/adr/) | [ADR v2.0.0-rc.2 (versie ter vaststelling)](https://logius-standaarden.github.io/API-Design-Rules/) | [API-Design-Rules](https://github.com/Logius-standaarden/API-Design-Rules) |
| [NLGov OAuth 2.0 profile (OAuth)](https://forumstandaardisatie.nl/open-standaarden/nl-gov-assurance-profile-oauth-20) | [OAuth v1 (definitief)](https://gitdocumentatie.logius.nl/publicatie/api/oauth/) | [OAuth v1.1.0 (werkversie)](https://logius-standaarden.github.io/OAuth-NL-profiel/) | [OAuth-NL-profiel](https://github.com/Logius-standaarden/OAuth-NL-profiel) |
| [NLGov OpenID Connect profile (OIDC)](https://forumstandaardisatie.nl/open-standaarden/nl-gov-assurance-profile-oidc) | [OIDC v1.0.1 (definitief)](https://gitdocumentatie.logius.nl/publicatie/api/oidc/) | [OIDC v1.0.1 (werkversie)](https://logius-standaarden.github.io/OIDC-NLGOV/) | [OIDC-NLGOV](https://github.com/Logius-standaarden/OIDC-NLGOV) |
| Kennisplatform API's modulen|[Stabiele modules, 21 december 2023](https://github.com/Geonovum/KP-APIs/blob/master/README.md) | nvt | [Kennisplatform APIs](https://github.com/Geonovum/KP-APIs) |
| CloudEvents|[Vastgestelde versie, 5 juli 2022](https://gitdocumentatie.logius.nl/publicatie/notificatieservices/CloudEvents-NL/) | [Werkversie, 5 juli 2022](https://gitdocumentatie.logius.nl/publicatie/notificatieservices/CloudEvents-NL/) | [NL-GOV-profile-for-CloudEvents](https://github.com/Logius-standaarden/NL-GOV-profile-for-CloudEvents) |
| Verwerkingenlogging|Nog in ontwikkeling | @@@ link vng | nntb |


### Nut

De overheid ontsluit gegevens en applicaties steeds vaker met standaarden. Voorbeelden hiervan zijn te zien op de website developer.overheid.nl, in Common Ground, Haal Centraal en het Digitaal Stelsel Omgevingswet.

Representational state transfer (REST) is een ontwerpprincipe dat wereldwijd veel gebruikt wordt voor het bouwen van programmeerinterfaces over het web (API's). REST is geen standaard maar een ontwerpprincipe, en laat nog veel vrijheid in het structureren van API's.

Deze standaarden maken het voor ontwikkelaars gemakkelijker om betrouwbare applicaties te ontwikkelen met API's van de overheid.

### Werking

Een application programming interface (API) is een gestructureerd en gedocumenteerd koppelvlak voor communicatie tussen applicaties. Zo lang er computers zijn, bestaan er API's en worden er verschillende API technologieën gebruikt. Sinds 2004 heeft Representational state transfer (REST) zich ontwikkeld tot een bepalend principe voor het realiseren van API's.
Zogenaamde ‘REST-API's’ doen voor applicaties wat websites voor mensen doen.
Websites presenteren informatie aan mensen, REST-API's maken applicaties en gegevens over het Internet beschikbaar voor andere applicaties. De technologie achter websites en REST-API's heeft daarom veel gemeen.

De overheid gebruikt REST-API's voor koppelingen met andere overheden, bedrijven en indirect ook met burgers, bijvoorbeeld via mobiele apps en webapps die aangeboden worden door bedrijven of overheden zelf.
Ontwikkelaars kunnen deze REST-API's bevragen vanuit de gangbare programmeertalen en frameworks zoals Python, Java, Microsoft C\#, PHP.

### Status

De statussen van de verschillende API standaarden zijn in de standaarden zelf vastgelegd. De Status van dit beheermodel is als volgt:

| Gremium | status | toelichting |
| ------- | ------ | ----------- |
|Technisch Overleg | Concept akkoord | Operationeel gezien wordt deze nieuwe versie van het beheermodel besproken in de Technische overleggen die er voor de verschillende standaarden zijn. De concepten die in dit beheermodel worden gebundeld zijn op zich allemaal al akkoord. Het gehele definitieve document nog niet. |
|Mido|In behandeling|Het algemene Logius beheermodel waarop dit beheermodel is gebaseerd is al akkoord. De vraag ligt voor bij de PTGU om ook voor de API standaarden dit beheermodel te gaan volgen.|
|Forum Standaardisatie|Deels in behandeling|De ADR wordt als eerste opnieuw aangeboden bij het Forum en daar zal het beheermodel in worden meegenomen. Daarna volgt OAuth en dan OIDC|

## BOMOS

Het activiteitendiagram toont welke lagen het model onderscheidt en welke activiteiten daarbinnen onderscheiden worden. De lagen en de ondersteunende
activiteiten worden elk in een hoofdstuk besproken.

![BOMOS activiteitendiagram](images/bomos_activiteiten.png "BOMOS activiteitendiagram")

Voor meer details of BOMOS verwijzen we naar de documentatie: [BOMOS, het fundament](https://gitdocumentatie.logius.nl/publicatie/bomos/fundament/) en [BOMOS, de verdieping](https://gitdocumentatie.logius.nl/publicatie/bomos/verdieping/)
