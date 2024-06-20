# Creators Update 2 Microsoft Edge Google Inet_e_resource_not_found


# Creators update
## The issue
Since the Creators Update navigating to any Google site (google.com, google.co.uk, google.nl, etc.) results in an INET_E_RESOURCE_NOT_FOUND error, only on my work laptop, none of my other devices which I've also upgraded.

This *only* happened with Google, no other site had this issue... furthermore I could reach Google(.com) fine via Ping from commandline, Internet Explorer, FireFox and Chrome...

Cleared my (Edge) browser cache, history, etc. no results. Everything was working fine until the Creators Update.

I reported the issue via the Feedback Hub, ~~but obviously that's no guarantee~~ that I would have my Edge browser working with Google as my default search engine... and I so much like Edge with Google as the default search engine!

## Event Log
So I started to pick through my Event Log one error at a time, fixing minor issues every step of the way. Including the following DCOM error, specifically for the RuntimeBroker service:  
"*The application-specific permission settings do not grant Local Activation permission for the COM Server application with CLSID {D63B10C5-BB46-4990-A94F-E40B9D520160} and APPID {9CA88EE3-ACB7-47C8-AFC4-AB702511C276} to the user NT AUTHORITY\LOCAL SERVICE SID (S-1-5-19) from address LocalHost (Using LRPC) running in the application container Unavailable SID (Unavailable). This security permission can be modified using the Component Services administrative tool.*"  
![DCOM](/images/2017/04/DCOM-300x197.png)

As a SharePoint consultant I come across this type of DCOM error quite regularly:  
https://support.microsoft.com/en-us/help/920783/event-id-error-messages-10016-and-10017-are-logged-in-the-system-log-after-you-install-windows-sharepoint-services-3.0

## The fix
In order to fix the error, first take ownership (right click, permissions, advanced, take ownership) of the following registry keys via RegEdit:

* HKEY_CLASSES_ROOT\AppID\\{9CA88EE3-ACB7-47c8-AFC4-AB702511C276}
* HKEY_CLASSES_ROOT\CLSID\\{D63B10C5-BB46-4990-A94F-E40B9D520160}

Then ensure you provide the SYSTEM account with local launch & local activation permissions, refer to the Microsoft Support link above if you need specific steps to do so. When prompted that editing these permissions requires you to remove an unrecognized account from the permissions list, click remove. Since the application wasn't functioning properly anyway I figured... what the hell... and it's working fine right now.  
![DCOM 2](/images/2017/04/DCOM_2-300x205.png)

After ~~fixing this~~ I also noticed the login screen no longer waits 5 seconds before accepting my PIN, ~~two for the price of one~~!

## Update #1
**UPDATE 19-04-2017:**
Apparently I was too quick in releasing my post, above did not fix the Google issue. (it *did* however fix the slowdown in accepting my PIN)

As provided by Microsoft the issue can be worked around in two ways until they release a fix:

* Type about:flags in the address bar. Scroll down to the Networking section (near the bottom) and uncheck Enable TCP Fast Open, *then restart the browser*
* Use InPrivate Browsing when using Edge.

What the feature does:  
[https://www.windowscentral.com/enable-tcp-fast-open-microsoft-edge-faster-page-load-times](https://www.windowscentral.com/enable-tcp-fast-open-microsoft-edge-faster-page-load-times)

I did disable this feature, I just didn't restart my browser afterwards... this led me to believe the above fix actually resolved my issue. **Kudo's to Microsoft** for providing a workaround via the Feedback Hub!
