# SfB HA SQL DAG Configuration


**One of those silly mistakes…** As mentioned in my [previous post]({{< ref "/posts/customers-dont-have-a-frakking-clue" >}}), I’ve recently installed and configured a new Skype for Business landscape at my company. While implementing this I made one of those silly mistakes that cause you to spend hours looking for a solution… which is in fact one simple undocumented configuration setting. For our SfB configuration we use a high availability SQL cluster and we’ve also set up a Database Availability Group, or DAG. Once enabled, the first field gets relabeled ‘SQL Server Availability Group Listener FQDN’, the second ‘SQL Server FQDN’. Initially before enabling the DAG I set these values:

* Field 1, SQL Server DAG FQDN;
* Field 2, any given SQL Server node FQDN which will become part of the DAG. 

Which looks like this:  
![DAG before](/DAG_Before.png)

After the installation was complete and my published topology was running I ran into all sorts of problems, the root of which was the SQL datasource being read-only. Shortly after I determined the errors went away for a while when I switched the active node in the SQL cluster, so *something* had to be wrong with those settings… **but what**?!

# The fix
So what’s the correct configuration? After the initial installation of SfB *and* finalizing the replication of all the databases for the SQL DAG, **you need to change the SQL server FQDN back to the DAG FQDN.**

* Field 1 requires, SQL Server DAG FQDN;
* Field 2 requires, SQL Server DAG FQDN.

![DAG after](/DAG_After.png)

Why are there two fields for the same setting? You need to install the databases onto a single SQL node once before you can switch on the DAG settings, ***then remember to reconfigure the SQL store in your SfB topology with the DAG FQDN***. Would be nice if the Microsoft documentation was explicit on the little things like these. One final tip, whenever you see a field that requires the **FQDN**, double check you *actually used the FQDN* before publishing your topology. Changing the FQDN on the SQL Server store after the topology has been published can be a chore…
