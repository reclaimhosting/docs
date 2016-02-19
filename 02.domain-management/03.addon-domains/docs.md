---
title: 'Addon Domains'
taxonomy:
    category:
        - docs
---

##What is an Addon Domain?

An addon domain is a term that cPanel uses for adding another domain to your hosting account. An Addon Domain basically tells the server "I own this domain and now I want to host it on this server and do something with it." 

While a subdomain is a branch off of your current domain (i.e. test.yourdomain.com), an addon domain is a separate, fully functional domain added onto the hosting account you already have (i.e. yourseconddomain.com)


##Obtaining an Addon Domain

You can buy a new domain name directly from us through your client portal by going to **Domains>Register a New Domain**:
<br><br>

![photo one](https://farm2.staticflickr.com/1529/24136347169_7c173260ae_z.jpg)
<br><br>
...or you can transfer a domain you have from another registrar to your Reclaim Hosting account. For this post, we'll go over how to set up a new domain (purchased from us) first, and go over how to transfer in a domain from another registrar at the end.

If you'd like to transfer a domain from another registrar, jump down to the **transferring a domain from another registrar** section of this tutorial.

##Setting up your new domain

For the purposes of this tutorial, let's say you just purchased javatuesdays.com as a second domain, and now you'd like to add it to your cPanel has a addon domain. 

After purchase, head to your cPanel, scroll down and click **addon domains**.
<br><br>
![photo2](https://farm2.staticflickr.com/1471/24478070156_100c1a88f1_z.jpg)
<br><br>
Next, type in your newly purchased domain in the **new domain name** field. (The **subdomain** and **Document Root** fields will populate automatically.) In our case, I am going to remove the ".com" from my "Document Root" folder, but that is only for my convenience when using FTP, you do not need to do this.
<br><br>
![photo3](https://farm2.staticflickr.com/1634/24478142696_37203a84d2.jpg)
<br><br>
**Note**: You also have the option of creating a new FTP account that has access to the content on your domain. You also do not need to do this, but you may want to if you'd like to give someone else FTP access to your site. Your existing FTP credentials will allow you to get access to all of your Reclaim sites.

Once you're done setting up your domain options, click **Continue** and wait a few seconds for your changes to process. That's pretty much it!

##Installing applications on your addon domain

Once your domain is set up, you can select and install applications like WordPress or Omeka like normal. Find out how to get started with WordPress [here](http://docs.reclaimhosting.com/getting-started/installing-wordpress), or learn to work with Omeka [here](http://docs.reclaimhosting.com/omeka/installing-omeka).

##Transferring a domain from another registrar

Transferring a domain you already own is not too much different from registering a new domain, except the transfer process requires an **EPP code**, or an agreement code obtained from your registrar that allows the registrar to release your domain. 

Head to your Client Area and click **domains > transfer domains to us**. 
<br><br>
![photo4](https://farm2.staticflickr.com/1662/23876357554_00e1a618ff.jpg)
<br><br>
You will be prompted to enter your EPP code on the same screen where we ask if you'd like to buy the identity protection. 

**How to find your EPP Code**:

[Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/258/84/what-should-i-do-to-transfer-a-domain-from-namecheap) (they provide some of the most comprehensive info on this process, if you're interested)

[Godaddy](https://www.godaddy.com/help/transferring-domain-names-to-another-registrar-3560 "Godaddy")

[Network Solutions](http://www.networksolutions.com/support/preparing-a-domain-name-for-a-transfer-out-of-network-solutions/)

[Hover](https://help.hover.com/entries/21194003-How-to-Transfer-your-domain-away-from-Hover)

At this stage, here are a few items to note:

* If you have whois protection enabled through your outside registrar, you must disable it temporarily before you initiate the transfer. This is because we will send an authorization email to confirm the email address paired with your domain. (This is a *"are you really sure you want to transfer?"* message.)
* You must click the confirmation link in the email we send, or you will have to start the process over!
* The domain must be older than 60 days. 
* The domain must have no other transfers in the last 60 days.
* The domain transfer process can take up to 5 days.

If your domain registrar doesn't appear here, you can do a Google search for "epp code" and then the name of your registrar. If you're still having troubles finding your EPP code, send a support ticket our way. 

**Once we confirm that your domain has successfully been transferred,** you can head back up to the **setting up your new domain** section of this tutorial to set it up as an addon domain.