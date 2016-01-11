![cPanel Database Tools](http://i.imgur.com/8QnQiln.png)

cPanel includes several tools for managing databases in your account. The **MySQL Database Wizard** is a quick way to create databases, database users, and associate the two. The **MySQL Databases** area will show you all the databases and users  you've created an help you manage the creation and deletion of them. But when it comes to management there are two tools that I use often for editing, searching, importing, and exporting content within your databases.

The first tool is built right into cPanel called **phpMyAdmin**. This is actually a third-party piece of software that cPanel has integrated into the control panel to manage your databases. You'll still create and delete databases and users with the previously mentioned database management areas, however phpMyAdmin shines at allowing you to see and modify the content within databases as well as good import and export options.

![Screenshot of phpMyAdmin](http://i.imgur.com/3CfluWa.png)

While the look and feel of phpMyAdmin hasn't changed much over the years, it does a good job of showing you what you need to know. A list of your databases is available on the left sidebar. Across the top are all the various tools to interact with the selected database from browsing or searching the data, running queries on the database, or backing up and restoring the database. You have the option of running commands on particular tables here as well as the entire database. While some of the terminology can tend towards complex jargon, I do find some of the tools pretty straightforward, this backup section for example:

![phpMyAdmin Backup Screen](http://i.imgur.com/23GNQnz.png)

Although phpMyAdmin can be convenient because it's built right into cPanel, there are also desktop applications that you can take advantage of for management of your databases. A popular one is [Sequel Pro for Mac](http://www.sequelpro.com/) (and best of all, it's **free**!). In order to use Sequel Pro or any tool external to cPanel, you'll need to give your internet connection permission to access the databases. This is done using the **Remote MySQL** section in cPanel. The way your computer's connection is identified is by its IP Address which is a unique address assigned to your computer by your network provider when you connect. You can find yours by going to [http://ip4.me/](http://ip4.me/) or even [asking Google](https://www.google.com/search?q=what+is+my+ip+address). Once you have your IP address you can enter it into the Remote MySQL section and you'll now have permission to connect to your databases from your internet connection. If your IP address changes you'll need to update it in that area.

![Remote MySQL](http://i.imgur.com/nijU9MO.png)

In Sequel Pro you can connect to individual databases by putting in credentials that have access to that database (as well as your domain as the host). Keep in mind this is **not** your cPanel username and password, rather the username and password for a **Database User** that has access to the database you want to manage. Once connected you can take advantage of the tools in Sequel Pro to manage your database in the same way as with phpMyAdmin.

![Screenshot of Sequel Pro](http://i.imgur.com/snr8Vz0.png)

![Database in Sequel Pro](/content/images/2015/12/Screen-Shot-2015-12-19-at-6-29-32-PM.png)