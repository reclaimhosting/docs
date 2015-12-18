If you have installation somewhere else on the web you'd love to migrate over, or an application in your account that currently isn't managed by Installatron, Installatron can import applications and take over management of them for you.

Let's start by looking at installs that might already be in your hosting account, but not currently managed by Installatron. You may have migrated your account manually and setup those files and databases yourself to get the application online. Installatron makes it easy to add an existing application from your account. You start by logging into cPanel and clicking on the application you'd like to import into Installatron:

![List of Applications](http://i.imgur.com/Oo9XNnA.png)

>Note: While you may find the application you want to import on the homepage of cPanel if it's featured there, you can also click "View More" to see the full list, and there are indeed a lot.

Once you've found the application you want to import instead of clicking the "Install" button you're going to click the dropdown beside it and choose "Import existing install"

![Import Dropdown](http://i.imgur.com/fc1wzm8.png)

Since we're assuming the application is already in your hosting account you'll select "From this account" as the location (we'll cover the other option later)

![Import from this account](http://i.imgur.com/tWnBBFX.png)

Now all you have to do is tell Installatron what the URL of the install is and it will automatically read the install information and import it into your account. Once that's done you can take advantage of all the great Installatron features with your application.

![Import Finalize](http://i.imgur.com/bVBcF1W.png)

Now if you've been using Reclaim Hosting since the beginning you may not have a need for that, however importing applications is not limited to applications that are already on our server. Assuming you have FTP information for a previous host you can actually import those installs too! Follow the same instructions to find the application you want to import and choose the second option "From a different account"

![Import from external account](http://i.imgur.com/Ab9k9jY.png)

For this to work you'll have to give Installatron FTP (File Transfer Protocol) credentials to you're old hosting account so it can migrate the information. By providing login information as well as the path to the files, Installatron can assume the privileges of your previous application and grab everything it needs to migrate.

![Source Install Information](http://i.imgur.com/Bo7I4X0.png)

![Destination Install Information](http://i.imgur.com/9aKHgL9.png)

Once your application is imported you'll have a hosted application on Reclaim Hosting powered with Installatron which you can use to automate updates and backups. Moving files and provisioning databases is so last year!