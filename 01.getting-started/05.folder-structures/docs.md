---
title: 'Folder Structures in cPanel'
taxonomy:
    category:
        - docs
---

### Top-Level Folder Structure

We utilize an industry-standard control panel for hosting called cPanel at Reclaim Hosting, which has a lot of great tools for managing your account. However one area that can be confusing is the folder and file structure of an account and what all those folders actually do.

![Screenshot of File Manager](http://i.imgur.com/baxKI65.png)

Your account will typically be provisioned on the server under the **/home/username** folder where **username** is your cPanel username. This folder is sometimes called the **top-level** or **root** of your account. An easy mistake to make is to upload files to that folder and expect them to show up on your website, however the root folder is *not* publicly accessible on the web. The root folder holds system folders for a variety of functions that cPanel relies on (which is also why you should never delete these folders). A few of them are below with explanations:

*  **application_backups** - Any locally stored backups from Installatron will be stored here.
*  **logs** - An archive of Apache access logs for your domain.
*  **mail** - You guessed it, email to local email accounts on your domain is stored here.
*  **public_ftp** - This folder is not often used except for instances where you need a space to allow FTP users to upload files that aren't immediately public.
*  **public_html** - This is where the magic happens. This folder is the main folder for your domain that is accessible to the web. Files uploaded to this folder will be visible on your main cPanel domain.
*  **tmp** - Temporary uploads and statistics information is stored here.

As you can see, when uploading files to your account you'll likely want them to be in public\_html in order to be accessible on the web. So if a file **image.jpg** is uploaded there it will be available at **yourdomain.com/image.jpg**. Likewise, if you create a folder inside of public_html and add the same image there it would be accessible at **yourdomain.com/foldername/image.jpg**. 

###Subdomains

![Subdomain Interface](http://i.imgur.com/QtMkogO.png)

You can create subdomains in your cPanel account under the Domains > Subdomains area of cPanel. By default (and a recommended best practice) cPanel will create a folder for that subdomain that is *inside* public\_html and named after the subdomain (remember all files in public\_html are the ones publicly available on the web). cPanel calls this the **Document Root** for the subdomain. So if a subdomain **blog.yourdomain.com** is created cPanel will create a folder named **blog** inside of the public_html folder.

###Addon Domains

It is possible that you purchased a second or third domain and want to add it to your cPanel account. The interface for this is in cPanel under Domains > Addon Domains and is similar to the Subdomain interface in that cPanel will also create a Document Root for the domain (typically based on the name of the domain) inside the public\_html folder. So if I add **newdomain.com** as an Addon Domain, cPanel will create a folder named **newdomain.com** inside of public_html where I can now place files I want to host at that domain. Once a domain is added in Addon Domains it becomes available throughout cPanel for use, however the domain must be registered first either by Reclaim Hosting or with another domain registrar and the [nameservers](http://docs.reclaimhosting.com/Miscellaneous/Nameservers/) must point to Reclaim Hosting.

Learn more about Addon Domains [here](http://docs.reclaimhosting.com/Domain-Management/Addon-Domains/).
