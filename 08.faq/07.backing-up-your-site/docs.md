---
title: 'Backing Up Your Site'
taxonomy:
    category:
        - docs
---

Backing up your website allows you to create and design without fear of accidentally clicking the wrong button and losing your content. Reclaim Hosting supports a few different ways to do this: 

##### On-demand backups 
Directly in cPanel you have the option of generating a Full backup of your entire cPanel account (great for migrating to another service) or just your Home directory or databases. 

- Great option for getting a copy of your stuff as an export
- Manual solution that quickly may become out of date


##### Installatron backups
A large majority of our users make use of our automated installer in cPanel powered by Installatron to install WordPress, Omeka, and a host of other software. We often provide custom software packages through this plugin that aren’t typically easy to install on your own.

- Fast & simple
- Automated backup solution built in (You can choose whether to have a software backup on a scheduled basis, and/or any time there is an upgrade)
- Backups can be stored in a separate FTP location, or even somewhere like dropbox
- Choose the same location or different site to restore a backup 
- Backup includes all files and folders as well as the database for the install to get you back up and running quickly


The options mentioned above work just fine and offer security for the content you publish at Reclaim Hosting. However, they aren't your *only* options. On-Demand Backups and Installatron Backups don't allow you to quickly restore a single file or folder that may have been deleted or overwritten. Instead, you'd have to unpack a full backup to find what you were looking for. 


These backup solutions also default to storing the backups directly on the server which eats up your server space, and more importantly, is an insecure method of backing up content. Ideally you’d have a replicated copy of your stuff in an external location in case of larger issues with our datacenter or hardware that render the existing content inaccessible.

*Find the solution to these issues below*:

##### Automated Offsite Backups

Powered by R1Soft, we have now rolled out an off-site automated backup solution to all users that will capture a copy of all files and databases every day at noon and give you the power to restore them at a granular level directly from within cPanel. And best of all, this comes free of charge as a part of your account with us. Here’s how it works:

Directly from within cPanel you will find the R1Soft Backup Manager in the Files area. When you select it that will automatically redirect you to the offsite storage container for your content and log you in.

![Backing up your data](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-08%20at%2011.50.57%20AM_zpspn8kvpzl.png)

From there you will find several backups available to choose from. At this time you have chosen to store the last 10 days of your content. You can choose to either browse the folders within a particular backup to select specific content, browse your databases, download a full copy of the backup, or in extreme circumstances you can push a restoration of the entire backup back to your hosting account to revert every change that was made since the backup was created.

![Recovery Points](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-08%20at%201.09.52%20PM_zpsuuu3mbdk.png)

When browsing the contents of a backup you can granularly select specific files and folders that you want to recover. From the top menu you will have the option of either downloading a backup of the selected items, or restore those items back to your hosting account which will automatically push the items right back to your account and bring them online.

![Browse Recovery Point](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-08%20at%201.10.09%20PM_zpsu5jzcakq.png)

Automated offsite backups are available immediately in all accounts and provided free of charge to all of our customers.