---
title: 'Where Did All My Disk Space Go?'
taxonomy:
    category:
        - docs
---

Sometimes you may find that you just plain need more disk space. Perhaps you're regularly uploading large files to build an online archive for a project or you work with video files that need to be stored locally. As Reclaim Hosting has grown over the years we've consistently increased our storage options and luckily [upgrading is an easy process](http://docs.reclaimhosting.com/FAQ/Can-I-Upgrade:Downgrade-my-Account-Later/)! That being said we always encourage folks to diagnose the source of disk space issues to be sure there's not any other issues at play. Automated backups you weren't aware of in a folder on your account because of a plugin, or a log file that has grown rapidly could be the source and simply deleting a few files could free up large amounts of space in your account. But how to find that large needle in the haystack?

cPanel has a rudimentary tool in the control panel called **Disk Usage** which is found under the **Files** section. Disk Usage will calculate the size of every folder in your account and display it in a nice graph. However the biggest caveat that makes this a poor solution is that the Disk Usage tool will not let you navigate to subfolders. More often than not you'll find that the **public_html** folder which houses all your web content is the largest, but that could still leave you searching blindly for more information on where within that folder the culprit is.

![Disk Usage in cPanel](http://i.imgur.com/gx7Ag8Q.png)

![Disk Usage Detail View](http://i.imgur.com/YCLBQVM.png)

Because of the limitations of this tool we add a program to our servers called [Ncdu](https://dev.yorhel.nl/ncdu). Ncdu runs from the command line so you'll need to be logged in via terminal with your SSH account, however you'll find the interface pretty friendly. Once logged on simply navigate to the folder you want information about and type the `ncdu` command to get a text-based graphical representation of the largest folders.

![ncdu](http://i.imgur.com/1AFNCaI.png)

Because the folders and files are ordered by size I recommend starting at the root of your account and running the tool. You can use the arrow keys to move up or down and enter to navigate into a folder and get a readout of the size of its contents. In our experience it makes quick work of analyzing disk space issues and finding any opportunities to clear out the cruft. When you're finished simply hit the `q` key to quit. 

We've added **ncdu** to many servers but if for some reason it's not available in your account on Reclaim Hosting put in a support ticket and we'd be happy to make sure it gets added.