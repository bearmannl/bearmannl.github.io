# Custom Domain Names With Azurewebsites


I've only recently set up this blog and since it's always busy at work, I don't always have the time to sort out those 'nice to haves'. I'm hosting this blog using AzureWebsites, but obviously I use my own domain name. My pain? For the life of me I couldn't figure out the magic rule to rewrite my x.azurewebsites.net url to the proper 'bearman.nl' hostname I'm using now. Shame on me, Microsoft consultant couldn't figure out a simple IIS redirect rule... In my defense, I hadn't really taken the time to do it properly and I had in fact solved it, but in the wrong order. To setup an AzureWebsite using a custom domain you need to configure it in several places:

* In the Azure portal;
* DNS records with your domain registrar;
* In your application, in my case WordPress;
* An IIS rule to do the actual rewrite/redirect.

Where to configure in Azure? In the Azure Portal find your Web App settings and under the Routing header click on Custom Domains and SSL. Select Bring External Domain and follow the instructions. Pay attention to using the correct type of DNS records, A records and CNAME records, depending on the correct entry. With your domain registrar find the DNS Manager to actually enter the records. You need to set the awverify.*.azurewebsites.net record with a CNAME to verify your custom domain with Azure. I went and created an A record for my domain to the AzureWebsite. Most registrars provide a warning stating you need to wait a maximum of up to 24 hours before the records are updated, in my case they were available within a minute, this may vary based on the receiving location however. In your application add your custom domain, in the case of WordPress go to General Settings and edit your WordPress Address (URL) and Site Address (URL) accordingly. Finally comes the last bit of magic, the IIS rewrite rule. Kudo's to the [author of the solution](http://onthecloud.azurewebsites.net/seo-tip-how-to-block-the-.azurewebsites.net-domain) for the final makeup of the IIS rule and [DevJev](http://www.devjev.nl/) for nudging me in the right direction :-)  
```xml
<?xml version="1.0" encoding="UTF-8"?>
    <configuration>
        <system.webServer>
            <rewrite>
                <rules>
                    <rule name="Disable Azure Domain" patternSyntax="Wildcard" stopProcessing="true">
                        <match url="*"/>
                            <conditions logicalGrouping="MatchAll" trackAllCaptures="false">
                                <add input="{HTTP_HOST}" pattern="*.azurewebsites.net"/>
                            </conditions>
                        <action type="Redirect" url="http://www.mysite.com{REQUEST_URI}" redirectType="Permanent"/>
                    </rule>
                </rules>
            </rewrite>
            ...
        </system.webServer>
    </configuration>
```

So why couldn't I figure this last bit of magic out on my own... I tried to set this up *before completing the other steps*. Working on this yourself? Sort your Azure, DNS and WordPress config first!
