# Firewall Port Status Test Script


Recently I had some issues at a customer project where, due to the complexity of the environment, sometimes firewall ports were closed after they had initially been added to the rules list. This caused unexpected errors for SharePoint, of which we were unaware at the time that these were due to firewall issues.

While analyzing the issue I came across the Test-NetConnection PowerShell command, which I used to manually verify the issue on one server. However when the time came to repeat the command on several servers I started automating things with my own script. Soon enough the project manager asked me if I could output the results of my script to Excel and send him the files by mail.

Logging into several servers to collate the results and manually mail them seemed like a task that could be handled better, so once again I started to redesign and automate the process.

What resulted is a script with which you can map out local servers and their outbound server connections by port numbers. You can then run the script (scheduled if you want) on each server locally and it will output to a .htm file. I've configured it to output it to an IIS hosted file, so the IT operations guys can check the firewall status remotely whenever they want.

Obviously scheduling a check to ensure firewall ports are still open is not ideal, but should you need it I hope my work will save you some effort!

* [Test-NetConnections.ps1](https://github.com/bearmannl/posh/blob/master/Scripts/Test-NetConnections.ps1)
* [Test-NetConnections.json](https://github.com/bearmannl/posh/blob/master/Scripts/Test-NetConnections.json)
