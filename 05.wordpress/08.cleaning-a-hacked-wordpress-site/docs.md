---
title: 'Cleaning a Hacked WordPress Site'
taxonomy:
    category:
        - docs
---

Not all WordPress hacks are equal, but understanding how the files that make up a WordPress install are organized will help with cleaning one up. So let's look at the directory structure and break it down.

![WordPress 4.4.1 Directory Structure](http://i.imgur.com/YOK6VYg.png)

Here we have a clean WordPress install that hasn't yet been setup. I know this because a file wp-config.php isn't present at the root directory. In addition to several files at the root of the directory that handle logging in, serving up content, and mail delivery, we also have 3 main folders: **wp-admin**, **wp-content**, and **wp-includes**. Here's a brief description of each:

**wp-admin** - When you login to the dashboard of WordPress you might notice the URL is /wp-admin. The wp-admin folder stores all WordPress files necessary to display and interact with the backend of WordPress.

**wp-content** - This is where the files and folders unique to this particular install will end up. Plugins and Themes have a place here as well as all images that are uploaded to WordPress.

**wp-includes** - General php classes and any javascript files and libraries that WordPress relies on are located here. 

In addition to all those files your WordPress install has a database. This is typically only going to be seen through an admin area of your hosting provider. At Reclaim Hosting we provide phpMyAdmin through cPanel to view the databases in your account. The database stores all of the actual content (your posts, pages, site information, etc). 

Knowing all of this we can start to understand what the unique aspects of a WordPress install are versus the files and folders that can easily be replaced. The unique content of a WordPress install consists of:

* A **wp-config.php** file that has our database information.
* A **wp-content** folder with our plugins, themes, and uploads.
* A **database**

That's surprisingly it! Everything else can be replaced with a fresh copy from [WordPress.org](https://wordpress.org/) and your site would still be there. So now we've narrowed down the number of potentially hacked files, but we can go even further. For example we know that plugins and themes are all available in the WordPress repository so we can download fresh copies of those as well (if you use premium themes or plugins you'd need to get access to those again of course). That can be a time consuming process but wouldn't you rather spend the time now getting this right? 

When cleaning up a site I also take that as an opportunity to check and see if there are any plugins or themes I don't need. For example if I'm running a non-default theme I can easily delete all of the TwentyX themes provided by WordPress. Remember we're trying to remove as many potential targets for exploits as possible.

Finally when all is said and done and you're back online the last thing to do is run a full scan of your install. I personally like the [Wordfence plugin](https://wordpress.org/plugins/wordfence/) which makes this a straightforward process and can also protect your install from future malicious activity. There are options to check all plugins and themes as well as files outside of your WordPress install in the Wordfence settings, both of which I recommend turning on before doing a scan.

Cleaning up hacked installs is never a fun process and with WordPress powering over 25% of the web now it's become somewhat a large target. But hopefully these tips help you understand how to get a site back online and cleaned up in no time.