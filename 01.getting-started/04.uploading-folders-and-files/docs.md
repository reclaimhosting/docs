---
title: 'Uploading Folders and Files'
taxonomy:
    category:
        - docs
---

Uploading content from your computer to your hosting account can be accomplished in many different ways. Here are some of the more common approaches to adding Files and Folders to your account.

* [Using the File Manager in cPanel](#filemanager)
* [Using an FTP client such as Filezilla or Cyberduck](#ftp)
* [Using WebDisk to mount a network folder to your computer](#webdisk)

Before we outline these approaches it's probably best to explain how the folder structure in your hosting account works. When you connect to your hosting account for the first time you'll see a handful of folders with a structure similar to the screenshot below:

![image](http://i.imgur.com/WnSdhqu.png)

Most of these folders are system folders used by cPanel for things like login credentials, e-mail accounts, and temporary files. The main folder that you'll likely need to work with is the **public_html** folder which is the folder that contains files you want to be served on your domain (you might notice that the **www** folder is a shortcut to that same public\_html folder and exists for legacy accounts that previously relied on it). Files uploaded into the public\_html folder will be accessible at the root of your domain. For example image.jpg would be viewable at **yourdomain.com/image.jpg**. Folders within your public_html folder will create "subfolders" onto your domain. An example of this would be a blog folder with an image.jpg file inside being viewable at **yourdomain.com/blog/image.jpg**.

###<a name="filemanager"></a>Using the File Manager in cPanel

Within your control panel you have access to a web-based **File Manager** which allows you to do basic functions like upload, download, and move the files and folders around within your account. When you open it for the first time you'll see a popup like the following:

![image](http://i.imgur.com/IWyD95V.png)

The default folder "Web Root" that is selected is the **public_html** folder mentioned previously. You can also choose to have the File Manager display hidden files such as .htaccess files and .git folders, and checking the last box will skip the popup in the future and use the default folder anytime the File Manager is chosen.

![image](http://i.imgur.com/FrTxd0v.png)

The File Manager has a variety of tools and functions listed across the top of the screen. When any of them are chosen the action will be taken on the active folder or file selected in the main window on the lower-righthand side. For example choosing a file and clicking the **Rename** icon will open a popup to rename that file. The left-hand sidebar is a navigation menu to expand subfolders and select any folder in the account for viewing within the main window.

**Note**: When performing any functions in the File Manager here, you are directly modifying your hosting account. Please use caution with functions like deleting files or folders. Mistakes made here could render your site inaccessible and there is no undo button.

###<a name="ftp"></a>Using an FTP Account such as Filezilla or Cyberduck

While the File Manager in cPanel is great for quick tasks, it is not as good at doing multiple tasks like uploading several folders full of files or making a lot of changes. In addition, the changes you're making there are live on the server. For that reason we often recommend working with an FTP client. FTP stands for **File Transfer Protocol** and there are a lot of applications that will work with it and connect to our server. [Filezilla](https://filezilla-project.org/) and [Cyberduck](https://cyberduck.io/?l=en) are just two popular free FTP clients, but any will work.

To connect to your hosting account you'll need to have a username and password. An FTP account is created for you when your hosting account is provisioned and the credentials are emailed to you (the username is typically the first 8 characters of the domain name). If you're unsure what the username and password are you can view them by logging into the [Reclaim Hosting Client Area](https://portal.reclaimhosting.com/clientarea.php), clicking **All Accounts**, **View Details** for the hosting account, and then navigating to the **Change Password** tab.

For the purposes of this tutorial we'll be using Filezilla as the interface but any program should have a similar set of options. The interface opens with multiple panes, the left side showing your local set of files (in this case the Desktop on this computer) and the right pane showing the remote set of files (since we're not connected to a server yet we don't have anything showing there). The top pane is the current status messages from the remote server and the bottom is a file queue that will show any files queued for upload or download.

![image](http://i.imgur.com/fdzBcfq.png)

To connect to the hosting account we want to create a new "Site" by clicking **File > Site Manager**.

![image](http://i.imgur.com/aNyJ6tP.png)

You can have multiple sites setup within an FTP client. If this is your first time using it this will probably be empty. Go ahead and click **New Site** to enter information specific to your account.

![image](http://i.imgur.com/i2TiNCl.png) 

Go ahead and give your site a name you'll remember in the sidebar. The following items relate to your account with Reclaim Hosting:

**Host**: This is your domain (without http://www) such as **yourdomain.com**

**Port**: If you're using **FTP** this will be 21 (most clients will adjust this for you). If connecting via **SFTP** which is more secure, this will be 22. *Note* that you can only use **SFTP** with your default cPanel account; if you have created a separate FTP user account, you need to use regular **FTP**.

**Protocol**: FTP and SFTP will both work

**Encryption**: This is not required. For secure transfers we recommend using **SFTP** as the protocol.

**Logon Type**: Normal (other clients may call this "Username and Password" or "Account")

**Username**: Your FTP username (typically the first 8 characters of your domain, if you created an FTP account within cPanel it will likely look more like an email address such as **ftpuser@yourdomain.com**)

**Password**: Your FTP password

For now the rest of the settings can be left to default. Go ahead and click connect and you should see a set of files and folders appear on righthand pane.

![image](http://i.imgur.com/xXBZAhY.png)

Once connected to your account you can upload local files and folders by selecting them and right-clicking on them. This will upload them to the folder you currently have open on the remote side. Keep in mind that files must be in the **public_html** folder in order to be accessible on the web. You can also go in the opposite direction and download folders and files by right-clicking and choosing **Download** to download them to the folder you're in locally. Other options like renaming or moving files and folders are available from the context menu when you right-click.

![image](http://i.imgur.com/bAGOisI.png)

Using this process allows you to edit and save your files locally and then upload copies to your hosting account, ensuring you always have a local backup of the changes you make. It's also a quick way to move a large set of files and folders to and from your account.

More information about setting up **FTP** is available from our [FTP documentation](http://docs.reclaimhosting.com/Miscellaneous/FTP-File-Transfer-Protocol/).

###<a name="webdisk"></a>Using Web Disk to mount a network folder to your computer

Another convenient way of working with the files and folders of your account is to mount a network drive using a tool called **Web Disk** in cPanel. Web Disk is a fancy name for a standard protocol called **WebDav** and functionality is built into most operating systems including Mac and PC. cPanel provides shortcut scripts to setup your computer with a network folder by clicking on the **Web Disk** icon in cPanel and then **Access Web Disk**. You'll need to know what operating system version you are using to download the appropriate script. Once you've run the script you'll be prompted for a username and password which would be the same as your FTP account. This will mount a network drive to your computer with full access to the folders and files on the server, allowing you to drag and drop, rename, and delete items as you would any other folder on your computer. If the script doesn't work, cPanel also provides the settings to connect manually below the download link.

![image](http://i.imgur.com/jyw0bVH.png)
