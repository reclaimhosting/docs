---
title: 'FTP (File Transfer Protocol)'
taxonomy:
    category:
        - docs
---

FTP (**File Transfer Protocol**) is a painless and simple way to transport and manage files over the Internet. Normally used to move large files at once, FTP is great for uploading website files onto a hosting account. 

FTP exchanges data using two separate channels: *command channel* and *data channel*. The *command channel* is resonsible for accepting client connections and handling the exchange of simple commands between FTP client and server. The *data channel* is responsible for exchanging data in the form of directory listings and file transfers. 

By default, all Reclaim Hosting users have a FTP account that's already been created for them upon sign up. 

![FTP accounts](https://farm2.staticflickr.com/1689/24046309923_35fec208e3.jpg)

**NOTE**: You must have the FTP client that you're working with already installed on your computer before moving forward. If you don't have Cyberduck (or FileZilla or CoreFTP) installed on your computer yet, do this now.

##### Opening a Connection

At the top of the Cyberduck window you'll see the option to open a connection. Click that button, and a dropdown screen will appear. 

If you're working in your default FTP account, we recommend you click the dropdown menu and select **SFTP (SSH File Transfer Protocol)** instead of *FTP (File Transfer Protocol)*. Both SFTP and FTP work essentially the same, but SFTP is more secure (among other things it runs on a different port and can’t be scanned by someone else on the network). The two methods use the same credentials and settings so you do not need to change anything else to use SFTP. 

However, if you're using an additional FTP account in cPanel that you've created, you'll need to click **FTP** in the dropdown menu. 

For purposes of continuing with this tutorial, we are going to assume that you are working with the main cPanel account that was already created. 

After selecting **SFTP (SSH File Transfer Protocol)** in the dropdown menu, fill in the server name as your domain name. Your username and password are your [cPanel credentials](http://docs.reclaimhosting.com/faq/resetting-passwords#ftp-cpanel-password). Next to **Port**, type **22**. Reference the example below:

![SFTP](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%201.49.07%20PM_zps16dmhof8.png)

Once everything is filled out, click **Connect**.

##### Transferring/Moving Files

The folders and files that you see in the Cyberduck window act like the Finder (Mac) or other file manager for your FTP server. Therefore, transferring files with Cyberduck simply involves dragging files from one window to another.

##### Uploading Files

1. Select file(s) in Finder.
2. Drag the selected files into the Cyberduck window.

##### Downloading Files

1. Select file(s) in the Cyberduck window.
2. Drag file(s) into the Finder window.

##### Managing Files in Cyberduck

By right-clicking on any of the files in the Cyberduck window, you'll be given quick access to Cyberduck's file management commands. These commands can also be found by searching through the Cyberduck menu located at the top of your desktop screen. 

Note: If you wish to **create a folder**, avoid using spaces in folder names. Dashes and underscores are much more web friendly.

##### Disconnecting

If you wish to disconnect from your FTP server, simply click **Disconnect** at the top right-hand corner of your Cyberduck window. 

##### Creating another FTP Account

If you wish to add another FTP account, start by clicking on the FTP Accounts icon under the files section of your cPanel dashboard. 

![Add FTP Account](https://farm2.staticflickr.com/1644/24725295691_47cb5570d7_z.jpg)

Create a username and password for this FTP account. The username will take the format of an email address (unlike SFTP where just the username is entered, for standard FTP accounts the full address is used)

After putting your username and password into the designated areas, you'll want to erase your login information from the directory box so it looks like this:

![Directory](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%2011.57.51%20AM_zpssi1ggcok.png)

If you leave your login information in the directory box ( /login ), this FTP account will only have access to the /login directory, not the entire public_html directory. 

After deleting your login information from the directory box, click **Create FTP Account**.

![Create](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%2012.04.34%20PM_zpsbseeettc.png)