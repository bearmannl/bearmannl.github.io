# Sharepoint ULS Log Files Empty


Ran into an annoying issue today where a SharePoint server was not writing trace log messages, the result was a log directory with 0 bytes logging files.

Incidentally I found a Event Log error with the code:  
"A Session "WSSUSAGESESSION15" failed to start with the following error: 0xC0000022"

Other posts mention adding the service account (or the WSS_WPG group) for the 'SharePoint Tracing Service' Windows Service to the administrators group, tested that, this indeed fixes the problem. However this does not conform to the principle of least privileged accounts.

Finally I found that the 'Performance Log Users' security group provides the correct permissions to allow a service to write trace log information.

* Added the service account using commandline "net localgroup "Performance Log Users" "domain\username" /add"
* Restarted the 'SharePoint Tracing Service' Windows Service, problem solved with least amount of privileges!

PS. Adding the WSS_WPG security group to the performance log users group *does not* solve the issue.
