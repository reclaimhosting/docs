Installing a piece of software like WordPress in your Reclaim Hosting account is a very simple process (hey look, [we even have a document on that](http://docs.reclaimhosting.com/Getting-Started-with-Reclaim-Hosting/Installing-WordPress/)!) but what's not always as clear is how you might *move* an installation to a different URL. A lot of folks get tricked into thinking they can just move the files to a new folder and it will work, but in fact WordPress stores URLs in the database that will break your site if you just move the files around. A much easier way to move a site to a new location is using the Clone Tool in Installatron. You'll find it by clicking on your install in cPanel and clicking this little guy right here:

![Installatron Screenshot](http://i.imgur.com/CjO8f76.png)

Installatron will read the existing install and prompt you to choose a location for the copy to go. If you've setup a subdomain ahead of time you can choose it from the dropdown menu for the domain, alternatively you could put it in a subfolder like in the screenshot below:

![Selecting a new location](http://i.imgur.com/OW7lWVd.png)

Installatron handles all the nitty gritty work of migrating databases and files so all you have to do to get started is hit the **Clone** button and you're off to the races. In just a few short seconds depending on the size of the install you'll have a complete copy of the site at a shiny new URL.

![Start Clone Tool](http://i.imgur.com/xH307x2.png)

![Cloning](http://i.imgur.com/ljegdRo.png)

![Clone Complete](http://i.imgur.com/ZW1fD3k.png)

Once you've verified everything migrated properly you can delete the former install by just clicking the **X** next to it. Alternatively I think the Clone Tool is an excellent way of setting up quick development spaces to test new plugins and themes, so feel free to use it to quickly fire up a copy of your site to a development space and play around. With just a few clicks you can have a carbon copy of your site ready to go.