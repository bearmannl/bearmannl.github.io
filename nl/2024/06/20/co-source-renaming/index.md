# Open Source - Inner Source - Protected Inner Source


# Protected Inner Source

## Intro
### Inner source
In het digitale tijdperk is softwareontwikkeling een belangrijke drijfveer van innovatie. Inner Source heeft in dit domein aan populariteit gewonnen. Het is een strategie die Open Source-praktijken toepast binnen een organisatie. In tegenstelling tot Open Source, is Inner Source niet openbaar. Het blijft beperkt tot één enkele organisatie. Deze benadering stimuleert collaboratieve softwareontwikkeling en co-creatie. Teams binnen de organisatie kunnen bijdragen, ongeacht afdelingsgrenzen. Inner Source bevordert een cultuur van transparantie en gedeelde verantwoordelijkheid. Het leidt tot verbeterde codekwaliteit en versnelde innovatie. Door Inner Source te benutten, kunnen bedrijven de collectieve expertise van hun werknemers inzetten. Ze kunnen dit doen terwijl ze hun eigen code beschermen.

Als je meer wilt lezen over Inner Source, voel je vrij om dat [hier op Wikipedia te doen](https://en.wikipedia.org/wiki/Inner_source).

### Access Modifiers
In C# bepalen zogeheten access modifiers (toegangsmodificatoren) de toegang tot de class (klasse) en haar members (leden). Ze zijn essentieel voor inkapseling. Public, protected, internal en private zijn de primaire modifiers. Elk dient een uniek doel. Public classes zijn toegankelijk vanuit elke andere class. Protected classes zijn toegankelijk binnen hun eigen class en door instances (instanties) van derived classes (afgeleide klassen). Internal classes zijn alleen toegankelijk binnen hun eigen assembly. Private classes zijn beperkt tot de bevattende class.

Om de exacte werking van access modifiers in C# te begrijpen, raadpleeg het [Microsoft Learn-artikel hier](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/access-modifiers#summary-table).

## De analogie: source delen strategieën en access modifiers
Access modifiers in C# kunnen vergeleken worden met strategieën voor het delen van broncode. Interne classes lijken op Inner Source; ze zijn toegankelijk binnen een organisatie. Overweeg het volgende:

* Open Source code is beschikbaar voor *iedereen*.
* Inner Source code is alleen beschikbaar *voor degenen binnen één organisatie*.
* Closed Source code wordt strikt beheerd, *alleen beschikbaar voor een specifiek ontwikkelteam*.
* In vergelijking zijn Public Classes *open voor iedereen*, zelfs uit verschillende assemblies (iedereen in de wereld).
* Op dezelfde manier zijn Internal Classes gesloten voor iedereen, *behalve voor classes in dezelfde assembly* (één organisatie).
* Tot slot zijn Private Classes gesloten voor iedereen, *behalve voor methoden in dezelfde class* (één ontwikkelteam/afdeling).

Deze analogie helpt te verklaren hoe het delen van code werkt in relatie tot verschillende niveaus van toegankelijkheid.

## Protected Inner Source
### Een nieuw concept
Protected Inner Source, iets wat ik tot nu toe nog nergens anders heb gezien, lijkt op Protected Internal Classes (Beschermde Interne klassen). Het is een hybride toegangsniveau. Het maakt delen mogelijk tussen bepaalde vertrouwde organisaties. Deze organisaties opereren onafhankelijk maar delen een gemeenschappelijke vertrouwensgrens.
* Derived Classes uit verschillende assemblies. Vergelijkbaar met afzonderlijke organisaties die nog steeds *gelieerd zijn aan dezelfde moederorganisatie*.
* Non-derived classes uit verschillende assemblies, niet-gelieerde organisaties hebben *geen toegang*.

![protected-inner-source-diagram](protected-inner-source.png)

### Specifieke toepassingen
Hoewel dit misschien niet van toepassing is op de meeste organisaties ter wereld, zijn er enkele specifieke voorbeelden:
* Overheidsorganisaties (rijksoverheid, veiligheidsregio's, EU, enz.) delen vaak (meer) vrijelijk dan de private sector.
* Private organisaties met complexe juridische structuren, die nog steeds vertrouwen delen tussen zusterbedrijven.
* Consortiums, in elke sector, moeten mogelijk samenwerken aan specifieke source code met vergelijkbare vertrouwensniveaus.
* Broncode met een lage eigendomswaarde, bijvoorbeeld verouderde applicaties die niet meer worden ondersteund. Een contracterend bedrijf kan toegang krijgen om het eigendom over te nemen voor specifieke doeleinden.

![protected-inner-source-gov-organogram](protected-inner-source_gov-nl.png)
*Let op! Dit is een voorbeeld van gekoppelde ministeries. Er is voor de blogpost geen validatie gedaan van vertrouwensniveaus en mogelijkheid tot delen van code binnen de rijksoverheid.*

### De voordelen
Protected Inner Source biedt meerdere voordelen:
* Het bevordert samenwerking zonder de veiligheid in gevaar te brengen.
* Het vermindert dubbel werk over organisaties heen.
* Het versnelt ook innovatie en ontwikkeling.
* Deze aanpak benut de krachten van meerdere entiteiten.
* Dit doet het terwijl de autonomie van elke entiteit behouden blijft.
* Het biedt traceerbaarheid bij het wijzigen van complexe oplossingen.

### Overwegingen voor implementatie
Het implementeren van Protected Inner Source vereist zorgvuldige planning:
* **Vertrouwen en Veiligheid**: Hoe gaan organisaties een vertrouwensrelatie opbouwen en onderhouden? Welke beveiligingsmaatregelen zijn nodig om gedeelde code tegen externe bedreigingen te beschermen?
* **Bestuur**: Wie beslist wat er gedeeld wordt en hoe bijdragen worden beheerd? Er kan een bestuursmodel nodig zijn waar alle partijen het over eens zijn.
* **Interoperabiliteit**: Hoe wordt de gedeelde code ontworpen om ervoor te zorgen dat deze gemakkelijk aanpasbaar is over verschillende organisatiesystemen heen?
* **Juridisch en Naleving**: Zijn er juridische of regelgevende overwegingen bij het delen van code tussen dergelijke entiteiten?

## Conclusie
Protected Inner Source kan de samenwerkende ontwikkeling voor vertrouwde organisaties revolutioneren. Het combineert de openheid van Open Source met de controle en bescherming van Inner Source. Dit model kan met name voordelig zijn voor overheidsorganisaties in de publieke sector. Het stelt hen in staat om middelen efficiënt en veilig te delen.

Vooral in een wereld waar ecosystemen steeds prominenter worden kan dit voordelig zijn. Stel je voor dat je geen talloze uren hoeft te besteden aan het opstellen van licentieovereenkomsten en geheimhoudingsverklaringen voor dergelijke partnerschappen. Bouw voort op vertrouwde relaties in strategieën voor het delen van broncode. Net zoals we jaren geleden begonnen met gefedereerde identiteiten in Identity and Access Management!

