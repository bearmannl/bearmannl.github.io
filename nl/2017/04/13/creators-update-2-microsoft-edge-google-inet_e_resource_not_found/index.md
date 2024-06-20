# Creators Update 2 Microsoft Edge Google Inet_e_resource_not_found


# Creators update
## Het probleem
Sinds de Creators Update leidt het navigeren naar een Google-site (google.com, google.co.uk, google.nl, etc.) tot een INET_E_RESOURCE_NOT_FOUND-fout, alleen op mijn werk-laptop, niet op mijn andere apparaten die ik ook heb geüpgraded.

Dit gebeurde alleen met Google, geen enkele andere site had dit probleem… bovendien kon ik Google(.com) prima bereiken via Ping vanaf de commandline, Internet Explorer, FireFox en Chrome…

Ik heb mijn (Edge) browsercache, geschiedenis, etc. gewist, maar zonder resultaat. Alles werkte prima tot de Creators Update.

Ik heb het probleem gemeld via de Feedback Hub, maar uiteraard is dat geen garantie dat ik mijn Edge-browser zou kunnen gebruiken met Google als mijn standaard zoekmachine… en ik vind Edge met Google als standaard zoekmachine zo fijn!

## Event Log
Dus begon ik mijn Event Log door te nemen, één fout tegelijk, en repareerde kleine problemen bij elke stap. Inclusief de volgende DCOM-fout, specifiek voor de RuntimeBroker-service: 
"*The application-specific permission settings do not grant Local Activation permission for the COM Server application with CLSID {D63B10C5-BB46-4990-A94F-E40B9D520160} and APPID {9CA88EE3-ACB7-47C8-AFC4-AB702511C276} to the user NT AUTHORITY\LOCAL SERVICE SID (S-1-5-19) from address LocalHost (Using LRPC) running in the application container Unavailable SID (Unavailable). This security permission can be modified using the Component Services administrative tool.*"  
![DCOM](/images/2017/04/DCOM-300x197.png)

Als SharePoint-consultant kom ik dit type DCOM-fout vrij regelmatig tegen:
https://support.microsoft.com/nl-nl/help/920783/event-id-error-messages-10016-and-10017-are-logged-in-the-system-log-after-you-install-windows-sharepoint-services-3.0

## De oplossing
Om de fout te herstellen, neem je eerst het eigendom (rechtsklikken, machtigingen, geavanceerd, eigendom nemen) van de volgende registersleutels via RegEdit:

HKEY_CLASSES_ROOT\AppID\{9CA88EE3-ACB7-47c8-AFC4-AB702511C276}
HKEY_CLASSES_ROOT\CLSID\{D63B10C5-BB46-4990-A94F-E40B9D520160}
Zorg er vervolgens voor dat je het SYSTEM-account lokale start- & lokale activeringsmachtigingen geeft, raadpleeg de Microsoft Support-link hierboven als je specifieke stappen hiervoor nodig hebt. Wanneer je wordt gevraagd dat het bewerken van deze machtigingen vereist dat je een onherkenbaar account uit de machtigingenlijst verwijdert, klik dan op verwijderen. Aangezien de applicatie toch niet goed functioneerde dacht ik… wat maakt het uit… en nu werkt het prima.
![DCOM 2](/images/2017/04/DCOM_2-300x205.png)

Na deze fix merkte ik ook dat het inlogscherm niet meer 5 seconden wacht voordat mijn PIN wordt geaccepteerd, twee voor de prijs van één!

## Update #1
**UPDATE 19-04-2017**:
Blijkbaar was ik te snel met het publiceren van mijn bericht, bovenstaande heeft het Google-probleem niet opgelost. (het heeft echter wel de vertraging bij het accepteren van mijn PIN opgelost)

Zoals door Microsoft aangeboden kan het probleem op twee manieren worden omzeild totdat ze een oplossing uitbrengen:

Typ about:flags in de adresbalk. Scroll naar beneden naar het gedeelte Netwerken (bijna onderaan) en vink Enable TCP Fast Open uit, start vervolgens de browser opnieuw op
Gebruik InPrivate Browsing bij het gebruik van Edge.
Wat de functie doet:
https://www.windowscentral.com/enable-tcp-fast-open-microsoft-edge-faster-page-load-times

Ik heb deze functie uitgeschakeld, ik heb alleen mijn browser daarna niet opnieuw opgestart… dit leidde mij tot de overtuiging dat de bovenstaande fix mijn probleem daadwerkelijk had opgelost. Kudo’s aan Microsoft voor het bieden van een workaround via de Feedback Hub!

