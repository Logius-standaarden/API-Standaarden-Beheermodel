# Operationeel

Operationeel beheer omvat volgens BOMOS het tekstuele beheer van de documentatie, het verzamelen van eisen en wensen en de vertaling daarvan naar wijzigingsvoorstellen. Verder omvat het operationele proces de besluitvorming en het versie- of release-beheer.

Het operationele wijzigingsproces is ingericht op Github. De omgeving die we ook gebruiken voor het beheer en de publicatie van de documentatie. In dit hoofdstuk wordt het operationele wijzigingsproces op hoofdlijnen beschreven. Voor details van de implementatie verwijzen we naar [[[#gebruik-github-in-het-beheerproces]]]

## Initiatie

Toevoegingen aan de API Standaarden zoals het toevoegen van een nieuwe module worden behandeld als introductie van een nieuwe standaard.

1. Uitbreidingen en aanpassingen in de standaarden in beheer bij Logius komen tot stand door participatie van de verschillende belanghebbenden.
2. Belanghebbenden kunnen op verschillende manieren participeren.
    1. op persoonlijke titel (het proces is volledig open)
    2. als lid van de Community
    3. als lid van één van de overleggen: het Technisch Overleg, de Programmeringstafel Gegevensuitwisseling of het OBDO.

## Wensen en Eisen

Wensen en eisen zijn aanpassingen op de bestaande API standaarden. Wijzigingsvoorstellen kunnen binnen komen via verschillende kanalen:

1. Rechtstreeks bij de beheerorganisatie, tijdens overleggen, via de website of mail
2. Bij de werkgroepoverleggen van de standaard en tijdens overleggen, via de website of mail

## Uitvoering en ontwikkeling (Wijzigingsproces)

Afhankelijk van de impact van een wijziging kan deze aangemerkt worden als een _patch_. Een patch is een kleine (tekstuele) wijziging die geen impact heeft op implementaties.

Een _wijziging_ is een aanpassing met impact op de werking of het proces van de API standaard. Waarbij nog een onderscheid gemaakt wordt tussen wijzigingen met kleine en met grote impact.

Patches en wijzigingen worden verzameld in een _release_. Een release is een nieuwe versie van de API standaard. Nieuwe releases worden regelmatig doorgevoerd en moeten worden goedgekeurd door het Technisch Overleg en, afhankelijk van de impact van een nieuwe release door een programmeringstafel. Een nieuwe release wordt bekrachtigd door het besluitvormend overleg.

### Wijzigingen

Onderstaand schema geeft een overzicht van de behandeling van een wijzigingsvoorstel in het beheerproces:

![Behandeling van een wijzigingsvoorstel in het beheerproces](images/Beheerproces.png "Behandeling van een wijzigingsvoorstel in het beheerproces")

Onderstaande stappen worden door de beheerorganisatie genomen om het proces te doorlopen:

1. Acceptatie van een wijzigingsvoorstel.
2. Labelen van een voorstel als groot/klein, aangeven van status.
3. Behandeling van een wijzigingsvoorstel.
4. Agendering voor een overleg.
5. Advisering vanuit overleggen.
6. Acceptatie van een wijzigingsvoorstel.
7. Doorvoeren van een wijzigingsvoorstel.
8. Publicatie van een wijziging in de komende release

### Patches

Een patch is een zeer kleine wijziging die geen impact heeft op de implementatie. Bijvoorbeeld tekstuele wijzigingen in de documentatie. De beheerorganisatie beoordeelt de impact van een wijziging en bepaalt daarmee of het een patch betreft (of een wijziging).

1. Beoordeling van een voorgestelde patch door de beheerorganisatie
2. Doorvoeren van de patch door de beheerorganisatie
3. Publicatie van een patch in een release

### Releases

De API Standaard zullen gezamenlijk en afzonderlijk onderhevig zijn aan beheer en onderhoud wat leidt tot nieuwe releases. Het vaststellen van nieuwe releases vindt plaats binnen het releaseplanningsproces. Het tactisch overleg is verantwoordelijk voor de juiste uitvoering. Hier komen alle belanghebbenden met verantwoordelijkheid voor de behoefte, effecten en impact op de bedrijfsvoering, informatievoorziening en ICT samen.

Voor nieuwe releases wordt uitgegaan van een aantal principes:

1. De standaard dient in principe zo stabiel te zijn dat
   nieuwe releases van de standaard bestaande implementaties van een
   oudere release niet tot migratie verplichten.
2. De standaarde wordt streefd ernaar om interoperabel (engels: backwards compatible) te zijn met voorgaande releases
   (interoperabele verandering).
   Bij wijzigingen waarin ook dit niet mogelijk is, vindt een expliciete
   afweging plaats van de geboden verbetering ten opzichte van het belang
   van bestaande implementatie (beperking impact).
3. Wijzigingsaanvragen kunnen door belanghebbenden worden ingediend
   bij de beheerder.
4. Het Technisch Overleg is verantwoordelijk voor de
   beoordeling van ingediende wijzigingsaanvragen, uitwerken ervan
   en de inhoudelijke (door)ontwikkeling van de te beheren API Standaarden.
5. De beheerder zorgt voor de voorbereiding van de
   releaseplanning.
6. Het tactisch overleg beoordeelt de releasevoorstellen en stelt
   het beleid en de roadmap van nieuwe releases
   vast in het releaseplanningsproces.
7. Bij het vaststellen van een nieuwe release kan het strategisch overleg
   uitspraken doen over het ondersteunen van oude releases.
8. Maximaal kunnen twee (opéénvolgende) releases van een API Standaard
    gelijktijdig de status „In Gebruik‟ hebben.
9. Op het moment dat het functionele toepassingsgebied van
    een API Standaard, waarvoor het pas-toe-of-leg-uit-regime geldt
    wijzigt, wordt dit voorgelegd aan Forum Standaardisatie en het
    OBDO zodat het regime kan worden bekrachtigd voor dit nieuwe
    toepassingsgebied.

### Impact van wijzigingen en versienummering

Afhankelijk van de impact van een wijziging of patch krijgt een release een nieuw versienummer. Het versienummerbeheer volgt principes voor semantische versienummering [en is beschreven in een bijlage](#versienummering)

De beheerorganisatie schat op basis van de wijziging of patch in welk nieuw versienummer noodzakelijk is.

## Status van de standaard

| **Afkorting** | **Status van de standaard** | **Beschrijving van de status** |
|      ---      |              ---            |               ---              |
| IO | In Ontwikkeling | Een nieuwe release van de standaard is "In Ontwikkeling" wanneer er met medeweten en medewerking van participanten aan gewerkt wordt en wanneer dit onderdeel of deze release nog niet voor de buitenwereld is gepubliceerd. |
| IG | In Gebruik      | Als een nieuwe release van de standaard gereed is, en is bestendigd door Forum Standaardisatie, stelt het Technisch Overleg de status 'In Gebruik' vast. Door deze vaststelling worden gebruikers en ICT-leveranciers opgeroepen deze nieuwe release op te nemen in software en in gebruik te nemen. |
| EO | Einde Ondersteuning | De standaardversie met de status "Einde ondersteuning" wordt niet meer ondersteund door de beheerder. De kennis en informatie voor vragen en support is bij de beheerder niet langer beschikbaar. |
| TG | Teruggetrokken   | De standaard krijgt de status "Teruggetrokken" indien een release van de standaard niet bruikbaar blijkt (bijv. vanwege implementatieproblemen). |

## Documentatie

Alle documenten m.b.t. de API standaarden en het beheer van de standaarden worden openbaar en zonder drempels voor gebruik, gepubliceerd op [logius.nl](https://www.logius.nl/domeinen/gegevensuitwisseling/api-standaarden) en onze [Github pagina's](https://github.com/Logius-standaarden). Logius publiceert tenminste de volgende documenten:

- Dit API Standaarden beheermodel
- De vergaderstukken van het Technisch overleg en overige besluitvormende gremia.
- De specificaties van de standaard
- De voorlopige specificaties van de nieuwe versie van de standaard.
