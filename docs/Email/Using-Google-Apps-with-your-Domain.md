Managing e-mail can be one of the harder parts of reclaiming your space on the web. While building a web presence is easier with modern applications like WordPress, the state of email clients and protocols is much less advanced. You'll have to grapple with getting your IMAP accounts setup and all the settings correct, webmail options are limited in functionality, and deliverability is always a concern with shared hosting servers.

Many users for this reason decide to use a service like [Google Apps](https://apps.google.com/) with their domain. Google Apps allows you to have email addresses based on your domain but completely powered by Google using Gmail as a webmail interface and connecting to any Google-supported client. Luckily it's absolutely possible to push mail to Google while still maintaining complete control of your domain for building out content on Reclaim Hosting. This is done by editing several **MX Records** which are a type of record for your domain that tells our servers who is in charge of handling email for the domain.

Google outlines the necessary records for setting up Google Apps on your domain at [https://support.google.com/a/answer/33915?hl=en](https://support.google.com/a/answer/33915?hl=en). Essentially we'll be editing the MX records to reflect the following:

<table class="nice-table">
      <tbody>
        <tr>
          <th><strong>Priority</strong></th>
          <th><strong>Mail Server</strong></th>
        </tr>
        <tr>
          <td>1</td>
          <td>ASPMX.L.GOOGLE.COM.</td>
        </tr>
        <tr>
          <td>5</td>
          <td>ALT1.ASPMX.L.GOOGLE.COM.</td>
        </tr>
        <tr>
          <td>5</td>
          <td>ALT2.ASPMX.L.GOOGLE.COM.</td>
        </tr>
        <tr>
          <td>10</td>
          <td>ALT3.ASPMX.L.GOOGLE.COM.</td>
        </tr>
        <tr>
          <td>10</td>
          <td>ALT4.ASPMX.L.GOOGLE.COM.</td>
        </tr>
      </tbody>
    </table>

To make these changes you'll log into cPanel and navigate to the **Email** section and choose **MX Entry**.

![Email Section in cPanel](http://i.imgur.com/7ImFKxj.png)

By default cPanel creates a single MX entry that points to your main domain as the server for email (so if your domain is hosted by Reclaim Hosting mail will be routed through the server your domain is on). We'll need to change that to take advantage of Google Apps for email. Each MX record has two items, a **Priority** number which tells the server which order to check for email records, and a **Destination** which is a domain that will serve the email.

![MX Entry Editing Interface](http://i.imgur.com/fmke3zE.png)

You'll need to edit the existing one (or remove it) and then add a few additional ones from the table above. When you're done the records should look like this:

![Completed MX Records](http://i.imgur.com/EmKI3YA.png)

You're all done! Keep in mind changing records can take 24-48 hours to begin working, though it typically will happen much sooner. Once the records have propagated globally all email will be routed to Google and you can use their system to handle all of your email functionality while still maintaining control of your domain from Reclaim Hosting.