Reclaim Hosting includes an automated installer for Omeka, an open source publishing platform with a focus on collections and repositories. Here are a few tips and tricks that can help make sure you get the most out of the software.

###ImageMagick

Omeka requires the ImageMagick library in order to resize and generate thumbnails for your images. Reclaim Hosting provides ImageMagic on all of our servers but occasionally you will need to manually enter the server path to the utility. The setting for this is located under the **Settings** > **General** tab and the path to ImageMagick is **/usr/bin**

![image](http://i.imgur.com/mIMQV8G.png)

###PHP-CLI

Some plugins may need to execute code using the command-line version of PHP. If your plugin requires this it can be enabled by editing **application/config/config.ini** and modifying the **background.php.path = ""** line to the following: **background.php.path = "/usr/bin/php-cli"**

###Uploading Plugins and Themes

Omeka provides a variety of open source themes and plugins on our website available for download, however there is no automated process for loading them into your Omeka installation from the admin interface at this time. Here's how to makes plugins and themes available to your installation.

Login to Reclaim Hosting and navigate to your cPanel via the menu

![image](http://i.imgur.com/078MlRC.png)

![image](http://i.imgur.com/9GULbFn.png)

In cPanel you'll be using the **File Manager** utility to navigate to the appropriate folder and upload the files.

![image](http://i.imgur.com/01jwC8o.png)

Within the File Manager you can navigate to your Omeka directory where you'll find a plugins and themes folder. Inside of those folders are the plugins and themes for your installation and you can upload and extract new ones using the built-in tools of the File Manager. You may also find our document on [using File Manager and other tools for managing files in your account](http://docs.reclaimhosting.com/Getting-Started-with-Reclaim-Hosting/Uploading-Files-to-your-Reclaim-Hosting-Account/) useful.