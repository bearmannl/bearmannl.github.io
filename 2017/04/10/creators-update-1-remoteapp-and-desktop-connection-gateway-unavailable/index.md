# Creators Update 1 Remoteapp and Desktop Connection Gateway Unavailable


Last week I upgraded all my personal Windows 10 devices to build 1703 (Creators Update) and after a few days of testing I was convinced this build is solid enough to upgrade my work laptop as well... true so far except for one minor issue! When I had to connect to a client's RemoteApp and Desktop Connection gateway, which they host on Windows Server 2008R2, I got the following error: "*Your computer can’t connect to the Remote Desktop Gateway server. Contact your network administrator for assistance.*" I don't know exactly what changed in this Windows build with regards to the RDP client, however I worked around it by restoring the following two files to the Windows System32 folder, from the Windows.old folder:  

* mstsc.exe
* mstsccax.dll

![MTSC replace](/images/2017/04/MSTSC_replace-300x300.png)

As you can see from the file replace details, the files have changed somewhat with this new build. I don't yet know if this also occurs with RDS hosted on 2012 and up, if it does please leave a comment below. Obviously not a permanent solution, but unfortunately I don't have the luxury of waiting for one.
