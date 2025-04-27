# Soevereiniteitsschaal: Een Pad naar Digitale Onafhankelijkheid van de EU


# Introductie van de Soevereiniteitsschaal: Een Pad naar Digitale Onafhankelijkheid van de EU

In het huidige digitale landschap wordt het concept van soevereiniteit steeds belangrijker, vooral binnen de Europese Unie (EU). Naarmate geopolitieke omstandigheden veranderen, groeit de vraag naar soevereine cloud- en technologische oplossingen die kunnen concurreren met de dominantie van Big Tech-bedrijven zoals Amazon, Google en Microsoft. Echter, de weg naar echte digitale onafhankelijkheid is complex en veelzijdig. Hier komt de Soevereiniteitsschaal in beeld—een nieuw concept ontworpen om de voortgang richting digitale soevereiniteit van de EU te meten en te bevorderen.

Voordat we dieper ingaan, laten we eerst begrijpen wat soevereiniteit letterlijk betekent:
1. "_hoogste macht of autoriteit_"
2. "_de autoriteit van een staat om zichzelf of een andere staat te besturen_"
3. "_een zelfbesturende staat_"

Deze definities helpen ons om een meer gestructureerde discussie over het onderwerp te voeren.

## Begrip van de Soevereiniteitsschaal

De Soevereiniteitsschaal is een raamwerk dat de soevereiniteit van de digitale systemen van een organisatie beoordeelt op een schaal van 0% tot 100%. Deze schaal helpt organisaties hun huidige niveau van digitale onafhankelijkheid te beoordelen, realistische doelen voor verbetering te stellen en te definiëren wat nodig is om die doelen te bereiken. Hier is een overzicht van wat de percentages betekenen:

- **0%-25%**: Minimale soevereiniteit. Organisaties in dit bereik zijn sterk afhankelijk van externe leveranciers voor hun digitale infrastructuur, software en diensten. In dit geval is een andere organisatie de _hoogste macht of autoriteit_ over de digitale infrastructuur van je organisatie.
- **25%-50%**: Basisgegevenssoevereiniteit. Deze organisaties hebben stappen ondernomen om de toegang tot hun gegevens te controleren, zoals het gebruik van Bring Your Own Key (BYOK)-oplossingen. Dit is een tussenpositie waarbij _de organisatie enige mate van autoriteit heeft om zichzelf te besturen_.
- **50%-75%**: Infrastructuursoevereiniteit. Op dit niveau hebben organisaties aanzienlijke controle over hun gegevens en compute-resources, mogelijk met behulp van hybride of multi-cloudoplossingen. Nog steeds een tussenpositie, maar _de organisatie heeft meer autoriteit om zichzelf te besturen_.
- **75%-100%**: Volledige soevereiniteit. Organisaties in dit bereik hebben volledige controle over hun software, hardware en diensten, vaak met behulp van open-sourceoplossingen en het hosten van hun eigen datacenters. In lijn met de letterlijke definitie is dit waar een organisatie een _zelfbesturende entiteit_ is.

### Wegingsfactoren

Hoewel ik persoonlijk het meest te maken heb met softwareapplicaties en platforms in mijn vakgebied, zijn de bovenstaande criteria op veel situaties van toepassing. Het zal ingewikkeld zijn om een specifieke soevereiniteitsscore voor alles in een organisatie te declareren.

Ik stel voor om relevante aspecten te evalueren, zoals al je IT-oplossingen op software-niveau, maar niet de hele toeleveringsketen, inclusief wie de upstream-kobaltmijn voor je technologische hardware bezit. Zodra je vakspecialisten in een enkel veld hebt die met die score komen, kun je altijd scores van verschillende niveaus aggregeren. Bijvoorbeeld, wat is onze hardware-engineeringsoevereiniteit versus onze software-engineeringsoevereiniteit?

Verschillende componenten van het digitale systeem van een organisatie kunnen verschillende gewichten hebben in de algehele soevereiniteitsscore. Bijvoorbeeld, gegevenssoevereiniteit kan voor sommige organisaties belangrijker zijn dan hardwaresoevereiniteit. Hier zijn enkele factoren om te overwegen bij het toekennen van gewichten:

- **Gegevenssoevereiniteit**: Controle over gegevens toegang en opslag.
- **Infrastructuursoevereiniteit**: Controle over compute-resources en hostingomgevingen.
- **Softwaresoevereiniteit**: Gebruik van open-source software versus propriëtaire oplossingen.
- **Hardwaresoevereiniteit**: Oorsprong en controle over hardwarecomponenten.

De volgende afbeelding illustreert hoe men conceptueel de schaal en de wegingsfactoren zou kunnen zien:

![soevereiniteitsschaal.drawio.png](soevereiniteitsschaal.drawio.png)

### Praktisch Voorbeeldscenario

Laten we de soevereiniteit van het cloudlandschap evalueren voor het fictieve bedrijf '**Dutch Hotels & Restaurants (DHR)**'. Dit bedrijf heeft verschillende fysieke hotels in Nederland, elk met restaurants. Ze bedienen veel klanten, communiceren intern met personeel en extern met klanten, verwerken betalingsinformatie en volgen strikte regels met betrekking tot fysieke veiligheid en beveiliging van hotelgasten. Hun cloudcomponenten omvatten:

| Product                                                            | Doel                                                                       | Bron          | Soevereiniteitsscore |
| ------------------------------------------------------------------ | -------------------------------------------------------------------------- | ------------- | -------------------- |
| SharePoint (Online)                                                | Administratieve bestandsdeling en opslag                                   | Closed Source | 10%                  |
| grommunio (zelf-gehost)                                            | E-mailserver                                                               | Open Source   | 80%                  |
| Microsoft Outlook (Desktopclient, cloudverbindingen uitgeschakeld) | E-mailclient-app op Windows                                                | Closed Source | 45%                  |
| Azure Virtual Machines                                             | Hosting van de openbare website, reserveringssysteem en grommunio          | Closed Source | 30%                  |
| Microsoft Teams                                                    | Interne communicatie                                                       | Closed Source | 10%                  |
| PostgreSQL-databaseservers (On-premises)                           | Hosting van databases met alle klantgegevens achter Azure-gehoste systemen | Open Source   | 90%                  |
| Site-to-site VPN                                                   | Connectiviteit tussen Azure-applicaties en databases on-premises           | Closed Source | 50%                  |

Voor het argument, laten we evalueren. Gemiddeld over deze basisscores krijgen we een **soevereiniteitsscore van 45%** voor het cloudlandschap in het algemeen.

Alle persoonlijk identificeerbare informatie (PII) en betalingskaartnummers worden opgeslagen in de on-premises databases. Dus vanuit de behoefte om _de gegevens van hun klanten te besturen_, is de 90% soevereiniteitsscore voor databases die on-premises worden gehost geweldig. De totale soevereiniteitsscore van 45% in die zin is misschien 'precies wat DHR nodig heeft'. Evenzo zorgt de e-mailserveroplossing ervoor dat alle communicatie met de klant strikt wordt gecontroleerd door DHR zelf, ook al zijn de servers geplaatst op Azure Virtual Machines.

Echter, als dit een grote federale overheidsorganisatie was, zouden ze misschien een minimale soevereiniteitsscore van 80% nodig hebben voor hun doeleinden.

De percentages zelf zijn op dit moment willekeurig, aangezien elke organisatie moet bepalen hoe ze deze in hun context berekenen. Als algemene richtlijn, overweeg de volgende aspecten voor het scoren van de soevereiniteit van een digitale oplossing:
- Gesloten/Interne/Open Source
- Transparantie van de leverancier (hebben ze en publiceren ze auditrapporten?)
- Roadmap van de leverancier (kun je de ontwikkeling beïnvloeden met functieverzoeken?)
- Is de leverancier onderdeel van je eigen jurisdictie/regio?
- Heeft de leverancier ooit significante beveiligingsincidenten gehad?
- Heeft de leverancier gerenommeerd personeel?

Door je systemen te taggen en te labelen met de relatieve soevereiniteitsscore, kan je organisatie een weloverwogen beslissing nemen over wat de totale score moet zijn (op strategisch niveau) en identificeren welke specifieke componenten mogelijk moeten worden gewijzigd.

Deze benadering kan helpen de kloof te overbruggen in discussies waar er polarisatie is tussen partijen die pleiten voor het volledig overstappen naar private cloud/open source of volledig publieke cloud met propriëtaire Closed-Source software. Het zal helpen de discussie te richten op wat je probeert te bereiken als specifiek doel.

## De Rol van Big Tech-bedrijven

Het is belangrijk om de aanzienlijke bijdragen van Big Tech-bedrijven te erkennen bij het bieden van volwassen en efficiënte oplossingen. Het doel van de Soevereiniteitsschaal is niet om deze bedrijven uit te sluiten, maar om een evenwichtige benadering te vinden die open-sourceoplossingen integreert waar relevant om de doelen van je organisatie te bereiken.

Hoewel het misschien eenvoudig lijkt om te zeggen: '_laten we alle publieke cloudsystemen vervangen door private cloud_', kan het een onoverkomelijke taak zijn als je organisatie niet de volwassenheid heeft om een private cloud te beheren. Bovendien hebben Big Tech-bedrijven het concept van hyperscale-datacenters verfijnd. Streven naar 100% soevereiniteit zou een zeer volwassen organisatie vereisen om hyperscale-datacenters te beheren, misschien zelfs je eigen chips voor de servers te ontwerpen en een volledig gecontroleerde inkoopketen tot aan de basismaterialen te waarborgen.

Kies een realistisch doel en erken dat sommige (zo niet alle) componenten nog steeds prima onder controle van Big Tech kunnen zijn, afhankelijk van je behoeften. Misschien kun je een volledig Microsoft Cloud (Microsoft 365/Azure)-omgeving gebruiken, maar volstaan met alleen overschakelen naar 'Bring Your Own Key' (BYOK) om 'volledige autoriteit over je eigen gegevens' te hebben.

Het nemen van incrementele stappen, zoals beginnen met BYOK en het implementeren van enkele on-premises servers die zijn verbonden via Azure Arc, kan je organisatie in staat stellen om 'vertrouwd te raken' met het nemen van soevereine controle over je systemen terwijl je leunt op de substantiële ondernemingsvolwassenheid van een Big Tech-bedrijf zoals Microsoft.

## Hybride/Multi-Cloud Benadering

Het bereiken van een gebalanceerde benadering van soevereiniteit via hybride of multi-cloudplatforms is niet nieuw. Al een decennium geleden, voordat soevereiniteit een modewoord werd, werd het als goede praktijk beschouwd om je organisatieportfolio te diversifiëren met hybride en multi-cloudplatforms. Organisaties kunnen open source-oplossingen hosten op infrastructuur van Big Tech, profiterend van de schaalbaarheid en kostenefficiëntie van deze aanbieders, terwijl ze geleidelijk overstappen naar meer soevereine oplossingen. Alternatief kun je uitsluitend gebruikmaken van Closed-Source software en -oplossingen, maar deze vrijwel uitsluitend hosten in privé-datacenteromgevingen.

Dit lijkt misschien een terugkeer naar de pre-cloudtijdperkoperaties, maar we hebben veel geleerd in de IT over het op een modernere manier beheren van onze systemen. Het is geen terugkeer als je een andere benadering hanteert voor privé-datacenters, bijvoorbeeld op een agile manier met CI/CD-praktijken die destijds niet gangbaar waren.

Het belangrijkste is de context. _Waarom wil je meer of minder soeverein worden op de soevereiniteitsschaal?_

## Win-Win Scenario

De hybride benadering kan een win-win zijn voor zowel EU-organisaties die meer zeggenschap willen over hun eigen IT-systemen als Big Tech-bedrijven die hun volwassen producten en diensten willen aanbieden. Big Tech-bedrijven kunnen relevant blijven door hostingdiensten aan te bieden voor open source-platforms en bij te dragen aan de ontwikkeling van soevereine oplossingen. Deze samenwerking kan EU-organisaties helpen om stapsgewijs richting soevereiniteit te gaan zonder volledig afscheid te nemen van Big Tech. Het kan verleidelijk zijn om te streven naar 'een volledig soevereine EU-cloud', maar overweeg de kosten en vereiste volwassenheid om dat punt te bereiken.

Vooruitgang boeken richting meer soevereine controle door EU-organisaties en Big Tech samen te laten werken is de meest realistische benadering, gezien alle betrokken factoren.

## Politieke en Economische Overwegingen

Het politieke en economische landschap is voortdurend in beweging. Het nemen van stapsgewijze stappen richting soevereiniteit stelt organisaties in staat zich aan te passen aan deze veranderingen en langdurige digitale onafhankelijkheid te waarborgen.

Gerichte discussies over hoe de soevereiniteitsschaal vooruit te bewegen (of niet, als je tevreden bent met de huidige situatie) zullen de kans vergroten dat dit werkelijkheid wordt.

## Conclusie en Oproep tot Actie

De Soevereiniteitsschaal is een hulpmiddel om de discussie rond digitale onafhankelijkheid te rationaliseren en weloverwogen beslissingen te nemen. Het moedigt organisaties aan om hun huidige niveau van soevereiniteit te overwegen en realistische doelen voor verbetering te stellen.

Om vandaag te beginnen:
- Definieer je strategische organisatiedoel voor soevereiniteit.
- Beoordeel je IT-landschap door elke digitale oplossing te labelen met een score.
- Identificeer componenten om hun respectieve scores te verbeteren.
- Overweeg bij het selecteren van verbeteringen of alternatieven de vereiste functionaliteitspariteit.
- Begin klein en bouw ervaring op door je soevereiniteit één component tegelijk te vergroten.
- Evalueer je voortgang regelmatig (per kwartaal/jaarlijks) en pas je doelen aan indien nodig.

Aan elke overheidsorganisatie die betrokken is bij het reguleren van onderwerpen zoals verplichte gegevensclassificatie, zou ik aanbevelen om soevereiniteitsclassificatie te overwegen. Hoe meer soevereiniteit wordt gelabeld, hoe specifieker discussies over het onderwerp kunnen worden gevoerd.

Je wordt uitgenodigd om je met dit concept bezig te houden, feedback te geven en je ervaringen met soevereine oplossingen te delen. Samen kunnen we bouwen aan een meer soevereine digitale toekomst voor de EU.

---

## Blijf Op de Hoogte

In de volgende blogpost zullen we dieper ingaan op concrete voorbeelden en marktverwijzingen, waarbij we illustreren hoe de Soevereiniteitsschaal kan worden toegepast in realistische scenario's. We zullen ook gedetailleerde specificaties geven over hoe soevereiniteitsscores voor oplossingen en systeemcomponenten kunnen worden berekend.

