# Gebruik GitHub in het beheerproces

## Publicatie

[GitHub](https://github.com/about) biedt functionaliteit om documenten te publiceren vanuit een repository. Logius gebruikt deze functionaliteit om het met [ReSpec](#gebruik-respec) gegenereerde document te publiceren als HTML-document en een PDF-document. Deze documenten worden automatisch gekopieerd naar een publicatiewebsite onder Logiusbeheer.

## Wijzigingsvoorstellen

Het proces zoals beschreven onder [operationeel beheer, wensen en eisen](#wensen-en-eisen) wordt voor de Logius standaarden geïmplementeerd door gebruik te maken van _GitHub issues_. Een _issue_ kan binnen GitHub ingediend worden
door iedere (GitHub)gebruiker en wordt bij ontwikkeling van code gebruikt om functionele wensen of gevonden bugs in te dienen zodat deze door ontwikkelaars opgepakt kunnen worden. Een _issue_ kan online besproken worden en uiteindelijk gesloten worden wanneer deze verwerkt is. Alle open en gesloten issue's blijven publiek inzichtelijk in de repository van de door Logius beheerde standaard.

### Branches

Binnen het standaardenbeheer bij Logius maken we gebruik van verschillende branches. De _main_ branch bevat de laatste formeel geaccepteerde versie van een document. De _develop_ branch bevat een werkversie met daarin alle wijzigingen die in een volgende geaccepteerde versie opgenomen moeten worden.

Aanpassingen in de documentatie die voor een specifiek wijzigingsvoorstel gemaakt worden worden in eigen branch verwerkt. Deze branch wordt gesplitst vanaf de _develop_ branch en wordt nadat het wijzigingsverzoek aangenomen is teruggebracht naar de _develop_ branch.

Voorbeeld: een wijzigingsverzoek voor het aanpassen van de architectuurbeschrijving zal in een branche _nieuwe architectuur_ worden verwerkt. Deze wordt gesplitst vanaf, en teruggebracht naar, de _develop_ branch. Door wijzigingen in een eigen branch op te nemen zijn alle wijzigingen op de documentatie inzichtelijk per wijzigingsvoorstel.

De _develop_ branch wordt dus niet gebruikt om wijzigingen op het document te maken maar dient als verzamelbranch voor de verschillende wijzigingen die in een volgende release moeten komen. _Patches_ kunnen wel direct op de _develop_ branch worden doorgevoerd.

### Commits

Commit messages zijn voor maintainers en derden belangrijk om een (historisch) beeld te krijgen van de evolutie van een standaard.
Om het onderscheid duidelijk te maken tussen normatieve en niet-normatieve wijzigingen, moeten commits met enkel niet-normatieve wijzigingen starten met _Editorial:_.
Probeer ook zoveel mogelijk wijzigingen te groeperen in commits die enkel normatieve wijzigingen toepassen en commits die enkel niet-normatieve wijzigingen bevatten.
Als deze worden gegroepeerd in (grote) commits, dan wordt het voor de lezer (en voornamelijk implementeerders) lastiger om te weten wat er in code moet worden veranderd om aan de standaard te voldoen.

Voorbeeld van een commit met enkel niet-normatieve wijzigingen:

   > Editorial: update copyright jaar

Voorbeeld van een commit met enkel normatieve wijzigingen:

   > Vereis dat alle URLs eindigen zonder een slash

Normatieve wijzigingen moeten geen prefix hebben en duidelijk uitleggen waar de wijziging over gaat, met in acht nemen van de generiek (Engelse) [guide voor het schrijven van bruikbare commit messages](https://cbea.ms/git-commit/).
In tegenstelling tot de gelinkte guide moeten commit messages in het Nederlands worden geschreven.

### Labels

Om GitHub issues te classificeren en te agenderen voor het juiste overleg maken we gebruik van een aantal standaard labels. We labelen binnenkomende issues als:

1. **Type** Alle soorten issues kunnen binnenkomen. Met Type sorteren we de issues in vragen, correcties en wijzigingen.
   1. Correctie
   2. Documentatie
   3. Vraag
   4. Wijziging
2. **Scope** Vooral relevant voor wijzigingsvoorstellen. Hiermee wordt aangegeven of het een kleine of grote wijziging betreft. Dit heeft betrekking op de impact van een wijziging en daarmee op de [versienummering](#versienummering).
   1. Klein
   2. Groot
3. **Overleg** Het label Overleg heeft alleen betrekking op wijzigingsvoorstellen. Wanneer deze labels gebruikt worden wordt het voorstel geagendeerd voor het betreffende overleg.
   1. TO-DK
   2. TO-Auth
   3. Gegevensuitwisseling
   4. Toegang
   5. Interactie
   6. Infrastructuur
4. **Status**
   1. In onderzoek
   2. In bewerking
   3. Uitwerking door derden
   4. In review
   5. Klaar voor review
   6. Gereed
   7. Afgewezen

## Automatisering en scripts

GitHub ondersteunt automatisering van taken door scripts. Standaard is de publicatie via _github pages_. Binnen de Logius standaarden maken we gebruik van scripts om documenten te publiceren, links te checken en om een paar eenvoudige tests op digitoegankelijkheidseisen uit te voeren.
