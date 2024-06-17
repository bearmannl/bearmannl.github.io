# Firewall Poort Status Test Script


Onlangs had ik wat problemen bij een klantproject waar, vanwege de complexiteit van de omgeving, soms firewallpoorten werden gesloten nadat ze aanvankelijk aan de regelslijst waren toegevoegd. Dit veroorzaakte onverwachte fouten voor SharePoint, waarvan we op dat moment niet wisten dat deze te wijten waren aan firewallproblemen.

Tijdens het analyseren van het probleem kwam ik het Test-NetConnection PowerShell-commando tegen, dat ik gebruikte om het probleem handmatig te verifiëren op één server. Maar toen het tijd werd om het commando te herhalen op meerdere servers, begon ik dingen te automatiseren met mijn eigen script. Al snel vroeg de projectmanager me of ik de resultaten van mijn script naar Excel kon uitvoeren en hem de bestanden per mail kon sturen.

Inloggen op verschillende servers om de resultaten te verzamelen en handmatig te mailen leek een taak die beter aangepakt kon worden, dus begon ik het proces opnieuw te ontwerpen en te automatiseren.

Het resultaat is een script waarmee je lokale servers en hun uitgaande serververbindingen per poortnummer in kaart kunt brengen. Je kunt het script vervolgens (gepland als je wilt) lokaal op elke server uitvoeren en het zal uitvoeren naar een .htm-bestand. Ik heb het geconfigureerd om het uit te voeren naar een door IIS gehost bestand, zodat de IT-operatiejongens de firewallstatus op afstand kunnen controleren wanneer ze maar willen.

Het is natuurlijk niet ideaal om een controle te plannen om te zorgen dat firewallpoorten nog open zijn, maar mocht je het nodig hebben, dan hoop ik dat mijn werk je wat moeite zal besparen!

* [Test-NetConnections.ps1](https://github.com/bearmannl/posh/blob/master/Scripts/Test-NetConnections.ps1)
* [Test-NetConnections.json](https://github.com/bearmannl/posh/blob/master/Scripts/Test-NetConnections.json)
