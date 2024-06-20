# Creators Update 1 Remoteapp and Desktop Connection Gateway Unavailable


# Creators Update
## Het probleem
Vorige week heb ik al mijn persoonlijke Windows 10-apparaten geüpgraded naar build 1703 (Creators Update) en na een paar dagen testen was ik ervan overtuigd dat deze build stabiel genoeg was om ook mijn werk-laptop te upgraden… tot nu toe waar, op één klein probleem na! Toen ik moest verbinden met de RemoteApp en Desktop Connection gateway van een klant, die ze hosten op Windows Server 2008R2, kreeg ik de volgende foutmelding: “Uw computer kan geen verbinding maken met de Remote Desktop Gateway-server. Neem contact op met uw netwerkbeheerder voor hulp.” Ik weet niet precies wat er in deze Windows-build is veranderd met betrekking tot de RDP-client, maar ik heb het omzeild door de volgende twee bestanden te herstellen naar de map Windows System32, vanuit de map Windows.old:

* mstsc.exe
* mstsccax.dll

![MTSC replace](/images/2017/04/MSTSC_replace-300x300.png)

## To be continued...
Zoals je kunt zien aan de details van het vervangen van de bestanden, zijn de bestanden enigszins veranderd met deze nieuwe build. Ik weet nog niet of dit ook voorkomt bij RDS gehost op 2012 en hoger, als dat zo is laat dan een reactie achter hieronder. Uiteraard geen permanente oplossing, maar helaas heb ik niet de luxe om op een te wachten.

