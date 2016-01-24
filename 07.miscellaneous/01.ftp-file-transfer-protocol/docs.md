---
title: 'FTP (File Transfer Protocol)'
taxonomy:
    category:
        - docs
---

FTP (**File Transfer Protocol**) is a painless and simple way to transport and manage files over the Internet. Normally used to move large files at once, FTP is great for uploading website files onto a hosting account. 

FTP exchanges data using two separate channels: *command channel* and *data channel*. The *command channel* is resonsible for accepting client connections and handling the exchange of simple commands between FTP client and server. The *data channel* is responsible for exchanging data in the form of directory listings and file transfers. 

##### Creating an FTP Account

To establish an FTP connection, you'll need to create an FTP account to which you can upload your files. To add a FTP account, start by clicking on the FTP Accounts icon under the files section of your cPanel dashboard. 

![FTP Accounts Icon](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%2011.31.59%20AM_zps2jgsempi.png)

Use you cPanel account's username and password to log in to FTP. If you're not sure where to find your cPanel password, click [here](http://docs.reclaimhosting.com/FAQ/I-Cant-Remember-My-Password/#ftp-cpanel-password).

After putting your username and password into the designated areas, you'll want to erase your login information from the directory box so it looks like this:

![Directory](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%2011.57.51%20AM_zpssi1ggcok.png)

If you leave your login information in the directory box ( /login ), this FTP account will only have access to the /login directory, not the entire public_html directory. 

After deleting your login information from the directory box, click **Create FTP Account**.

![Create](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%2012.04.34%20PM_zpsbseeettc.png)

##### FTP Configuration Files

The next step is to save all this information into files you can use to set up an FTP client on your local computer.

Now that you've created a FTP account, you'll see that account, plus other previous accounts you may have created in the past at the bottom of the *FTP Accounts* page. Click *Configure FTP Client* of the account that you would like to use.

![Configure FTP Client](http://i1071.photobucket.com/albums/u516/Brumface/Screen%20Shot%202015-08-26%20at%2012.09.18%20PM_zpsd4epamz1.png)

From there you will be given a set of choices for which client to use based off the type of computer you have. For purposes of this tutorial, we will be working with Cyberduck which works best with the Mac. 

![Client](http://i1071.photobucket.com/albums/u516/Brumface/86e1ff36-ec8a-47c2-b391-7f96f8f083df_zps0yfgiiyr.png)

**NOTE**: You must have the FTP client that you're working with already installed on your computer before moving forward. If you don't have Cyberduck (or FileZilla or CoreFTP) installed on your computer yet, do this now.

Now that you've installed Cyberduck, it's time to download the FTP Configuration and save it to your desktop. Do this by clicking the **FTP Configuration File** button underneath the Cyberduck icon. 

Next, double-click on the downloaded file, which here is located on the desktop. Cyberduck will open the download file and log you into your FTP account. If Cyberduck doesn't log you in automatically, use your cPanel credentials that you used earlier to create an FTP account. 

You now should see all of your website's content in Cyberduck. 

##### Opening a Connection

At the top of the Cyberduck window you'll see the option to open a connection. Click that button, and a dropdown screen will appear. 

If you're working with your main cPanel account, the one that was already created, we recommend you click the dropdown menu and select *SFTP (SSH File Transfer Protocol)* over *FTP (File Transfer Protocol)*. Both SFTP and FTP work essentially the same, but SFTP is more secure (among other things it runs on a different port and can’t be scanned by someone else on the network). The two methods use the same credentials and settings so you do not need to change anything else to use SFTP. 

However, if you're using data from an additional FTP account in cPanel that you've created, you'll need to use the regular FTP. 

For purposes of continuing with this tutorial, we are going to assume that you are working with the main cPanel account that was already created. 

After selecting *SFTP (SSH File Transfer Protocol)* in the dropdown menu, fill in the server name as your domain name. Your username and password are, again, your cPanel credentials. Reference the example below:

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

Note: If you wish to **create a folder**, avoid using spaces in folder names. Dashes "-" or underscores "_" are much more web friendly.

##### Disconnecting

If you wish to disconnect from your FTP server, simply click **Disconnect** at the top right-hand corner of your Cyberduck window. 
