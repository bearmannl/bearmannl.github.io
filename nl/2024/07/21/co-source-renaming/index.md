# Co Source - Hernoemde Source Code-deelstrategie


# Co source

## Intro
### Protected Inner Source Samenvatting
Protected Inner Source is een broncode-deelstrategie die een tussenmodel definieert tussen Open Source en Inner Source. De analogie die hier wordt gebruikt, is dat [C# Toegangsmodifiers ](https://learn.microsoft.com/nl-nl/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers#summary-table) een 'Protected Internal Class' definiëren als een tussenstap tussen 'Public Class' en 'Internal Class'. Het doel hiervan is om meer afgesloten te zijn tussen assemblies dan 'Public Class', maar meer open voor hergebruik dan 'Internal Class'.

Als je het vorige artikel wilt lezen, vind je het hier: [Open Source - Inner Source - Protected Inner Source](/nl/2024/06/20/open-inner-protected-source/)

## Broncode Deelstrategieën
Wat zijn broncode-deelstrategieën eigenlijk? Goed dat je het vraagt! :point_down:

Broncode-deelstrategieën verwijzen naar de verschillende methoden en praktijken die worden gebruikt om softwarecode te distribueren en samen te werken. Deze strategieën bepalen wie toegang heeft tot de code, hoe deze kan worden gewijzigd en het niveau van transparantie dat betrokken is. Het begrijpen van deze strategieën is cruciaal voor organisaties om hun softwareontwikkelingsprocessen effectief te beheren en samenwerking :handshake: en innovatie :bulb: te bevorderen.

### Soorten Broncode Deelstrategieën
1. **Open Source**: Deze strategie stelt iedereen in staat om de code te bekijken, te wijzigen en te distribueren. Het bevordert transparantie en samenwerking binnen de gemeenschap. Populaire voorbeelden zijn Linux en Apache. Meer over Open Source vind je [hier op Wikipedia](https://en.wikipedia.org/wiki/Open-source-software_movement).

2. **Inner Source**: Inner Source past Open Source-praktijken toe binnen een organisatie. Het stelt teams in staat om over afdelingsgrenzen heen samen te werken, terwijl de code privé blijft voor de organisatie. Deze aanpak verbetert de codekwaliteit en innovatie door gebruik te maken van interne expertise. Meer over Inner Source vind je [hier op Wikipedia](https://en.wikipedia.org/wiki/Inner_source) of [hier op GitHub](https://github.com/resources/articles/software-development/innersource).

3. **Closed Source**: Ook bekend als propriëtaire software, deze strategie beperkt de toegang tot de broncode. Alleen geautoriseerde individuen of teams binnen de organisatie kunnen de code bekijken of wijzigen. Deze aanpak wordt vaak gebruikt om intellectueel eigendom te beschermen en controle over de software te behouden. Hoe Closed Source zich verhoudt tot Open Source wordt in meer detail beschreven [hier op Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_open-source_and_closed-source_software).

4. :rocket: **Co Source** :rocket:: De nieuw voorgestelde hybride strategie die delen mogelijk maakt tussen bepaalde vertrouwde (of gefedereerde) organisaties. Deze organisaties opereren onafhankelijk maar delen een gemeenschappelijke :handshake: vertrouwensgrens :handshake:, vergelijkbaar met hoe Protected Internal classes werken in C#. Deze strategie bevordert samenwerking _zonder specifiek in te gaan op beveiliging binnen de OSS-ruimte_.

Elk van deze strategieën heeft zijn eigen set voordelen en uitdagingen. De keuze van strategie hangt af van de specifieke behoeften en doelen van de organisatie.

Voor een meer gedetailleerd overzicht van broncode en het beheer ervan, kun je de [Wikipedia-pagina over broncode raadplegen](https://en.wikipedia.org/wiki/Source_code).


### Naamswijziging naar Co Source
## Co Source Herintroductie
Ik ontving feedback op de naam '_Protected_ Inner Source'. Het leek te impliceren dat Open Source en Inner Source niet veilig zijn :lock:. Dit was (en is) niet de bedoeling!

Om een betere naam te vinden overwoog ik Federated Source, Trusted Source, Collaborative Source, Cooperative Source... uiteindelijk is het Co Source geworden. De term 'Co' suggereert zowel samenwerking als coöperatie. Dit past goed bij het idee van gedeelde broncode tussen vertrouwde entiteiten. Het houdt het ook schoon en netjes in dagelijks gebruik :smile:.

In de moderne IT-wereld veranderen veel aspecten van onze industrie door snel evoluerende (software) engineering innovaties. De snelheid waarmee dit gebeurt, is onder andere beïnvloed door Open Source-werkwijzen. Wat duidelijk is geworden, is dat deze werkwijzen een drastische impact kunnen hebben op het vermogen om in elk systeem te innoveren.

Bij het overbruggen van organisatieontwerp (vaak zakelijk gedreven) en systeemontwerp (vaak technologisch gedreven), kan Co Source veel voordelen bieden. Innovatie kan vooral veel profiteren, als een kernpijler achter het vermogen van organisaties om te veranderen. Het kan organisaties stimuleren om hun cultuur te veranderen op een manier die hen in staat stelt voorop te blijven lopen. Concurrentievoordeel gedreven door een cultuur van technologische innovatie.

Vooral binnen organisaties die IT niet als hun kernactiviteit hebben, kan het moeilijk zijn om zo'n cultuur aan te nemen. Toch brengt het zelfs voor strikt zakelijk gedreven organisaties enorme voordelen. Die impact is diepgaand, zoals Cloud ons de afgelopen 10+ jaar heeft laten zien en (Gen) AI in de afgelopen 1 a 2 jaar.

Aan die organisaties die moeite hebben om deze technologisch gedreven culturele veranderingen aan te nemen, zou ik adviseren om een cultuur rond Open Source-werkwijzen mogelijk te maken. Waarom? Het stelt individuen binnen die organisaties in staat om de voordelen te demonstreren met concrete levering van toegevoegde waarde door innovatie.

Naarmate meer individuen in de organisaties toegevoegde waarde en potentieel enorme impact op de winstgevendheid aantonen, ontstaat er een platform voor culturele groei.

Betekent dit dat de Open Source-werkwijzen specifiek in die vorm moeten worden aangenomen? Nee, dit is precies waarom Inner Source oorspronkelijk is bedacht.

Nu naar het punt van Co Source. Organisaties met complexe maar vertrouwde ecosystemen, zoals overheidsorganisaties, kunnen sneller tractie krijgen dan wat Inner Source binnen een enkele organisatie mogelijk maakt:
- Een culturele verschuiving naar technologische innovatie mogelijk maken.
- Aangetoonde toegevoegde waarde zien door levering van vroege innovatiescenario's.
- Dit proces opschalen door het succes van deze _golf van succes_ door technologische innovatiecultuur te omarmen.

## Beveiligingsimplicaties (of toch niet)
Nogmaals, Protected Inner Source was niet bedoeld om te impliceren dat Open Source niet veilig is. Er zijn beveiligingsuitdagingen bij elke strategie en die kunnen worden beheerd volgens de relevante situatie. Co Source moet nog steeds gebruik maken van best practices en goed ontwerpdenken passende bij de implementatie van deze strategie.

### Open Source en Inner Source Beveiligingsbest Practices
Aangezien Co Source werd geïntroduceerd om een nieuwe manier van werken binnen bepaalde organisaties of ecosystemen te introduceren, verwijs ik graag naar bestaande best practices in de OSS-beveiligingsruimte. Bekijk bijvoorbeeld het [OpenSSF](https://openssf.org/) artikel over [Strengthening Open Source Software: Best Practices for Enhanced Security](https://en.wikipedia.org/wiki/Comparison_of_open-source_and_closed-source_software).

## Voorbeelden en Toepassingen
Als specialist in #GovTech word ik voornamelijk gedreven door een visie van snel versnellende innovatie in de publieke sector. Binnen de publieke sector, in elk land zoals de Verenigde Staten of een groep landen zoals de Europese Unie, zijn er enorme potentiële voordelen te behalen door verhoogde samenwerking. Het omarmen van een cultuur van technologische innovatie is ten minste één manier om snel naar die potentiële voordelen te versnellen.

Hoe zou dit werken? Vanuit elke groep overheidsorganisaties, stel samenwerking op via Co Source repositories en begin toegevoegde waarde te demonstreren. Niet alleen toegevoegde waarde voor de (overheids)organisaties, maar ook voor de burgers die deze organisaties bedienen.

Zelfs concurrerende IT-leveranciers die binnen de publieke sector werken, kunnen het concept van [Coopetition](https://en.wikipedia.org/wiki/Coopetition) omarmen via Co Source. Door dit te doen, verbeteren we allemaal de impact die de publieke sector heeft op de samenleving als geheel.

## Conclusie
Co Source heeft het potentieel om collaboratieve ontwikkeling binnen een ecosysteem van vertrouwde organisaties te revolutioneren. Door de innovatieve aard van Open Source te combineren met de organisatorische grenzen van Inner Source, biedt Co Source een uniek model dat bijzonder voordelig kan zijn voor overheidsorganisaties in de publieke sector. Deze aanpak stelt deze organisaties in staat om middelen efficiënt en veilig te delen, waardoor een cultuur van samenwerking en innovatie wordt bevorderd.

In een wereld waar ecosystemen steeds prominenter worden, stelt Co Source organisaties in staat om voort te bouwen op vertrouwde relaties in broncode-deelstrategieën. Door een cultuur van samenwerking :handshake: en innovatie :bulb: te vestigen, kunnen organisaties technologische vooruitgang stimuleren en aanzienlijke voordelen behalen. Omarm Co Source om het volledige potentieel van collaboratieve ontwikkeling te ontsluiten en uw organisatie naar een toekomst van innovatie te leiden :rocket:!

