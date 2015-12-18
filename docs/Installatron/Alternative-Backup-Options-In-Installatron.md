Installatron has quite a few options for automating the process of backing up your site. Keeping regular backups is a safeguard against any number of issues that might come up from automatic updates that happen to be incompatible and break a site to malware or even changes made on accident. When you install an application on Reclaim Hosting using Installatron it is automatically set to backup anytime there's an update to the software. However you can also set a few interesting additional options either in the Advanced Options area during the install or by clicking this wrench icon on any of your existing installs:

![Accessing Install Details](http://i.imgur.com/X4sTxJI.png)

One of the cool features about Installatron is that you don't even have to backup an install to your own account. At Reclaim Hosting we store backups from Installatron on a separate server that doesn't count against storage quotas, but there are options here to store it in a variety of other locations as well, for instance in your [Dropbox](https://dropbox.com) account:

![Backup Storage Locations](http://i.imgur.com/RguXzCD.png)

You can also setup automated backups that happen at regular intervals, for example a daily and weekly backup of the account or some other set schedule so you have options to restore from:

![Automated Backup Intervals](http://i.imgur.com/YDPWtaI.png)

To demonstrate this I chose Dropbox as my backup location and clicked Save at the bottom of the screen. Upon saving a window prompts me to authenticate to Dropbox so Installatron has access to my account.

![Dropbox Access](http://i.imgur.com/sO3ABua.png)

After authorizing Dropbox to my account new backups will be stored as compressed files in my Dropbox account under a folder called **Apps/Installatron**

![Backing Up](http://i.imgur.com/ls2zVN5.png)

![Backup File](http://i.imgur.com/pG9BS8W.png)

This compressed file stores not only all of the files for that installation but also a complete copy of the database so you can take it with you to another hosting provider as well as restore a copy right from Installatron in the future if the need arises.