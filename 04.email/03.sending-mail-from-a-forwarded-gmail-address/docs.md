---
title: 'Sending Mail from a Forwarded Gmail Address'
taxonomy:
    category:
        - docs
---

Immediately after my last post for “Documentation December” on Forwarding Email in CPanel, I got a question about whether you can reply to messages sent to that email from the forwarded address. This is possible, and I will try and document the process with several email providers, but I’ll start with Gmail because that’s the one I use.

In order to send email from the forwarded address mail@jimgroom.com, I need to create an email account. This is not the case if you simply want to forward that email address to another account, but if you also want to send or reply to mail with this address you need to create an account. Click on the **Email Accounts** link in the Email section of CPanel.

![Email Accounts](http://imgur.com/0C4LQwV.png)

At that point you need to add an email account, and below is an example of how you can fill out the fields and then create the account. Keep the email quota low because you don’t want this to be storage, you will simply be using the email settings for this account to send them through Gmail.

![Email Settings](http://imgur.com/X7Ha47r.png)

Once the account is created you will see it listed under Email Accounts.

![Email Accounts](http://imgur.com/mRdtyTU.png)

Click on the **Configure Mail Client** link to get the settings you will need to add to Gmail. The settings you will need are your username, password, incoming server and SMTP port. Once you have those you are ready to head over to the Gmail account you’re forwarding this email to and go to **Settings**.

![Gmail Settings](http://imgur.com/CPVwxBO.png)

Once in settings, go to **Accounts and Import** and look for the **Send mail as** option. Then click on **Add another email address you own**.

![Account Import](http://imgur.com/gLEmAP3.png)

At that point you will see the following pop-up window, and you can add your name and the email address you are forwarding to Gmail. This should be the same email as the account you just created.

![Forwarding](http://imgur.com/k4waOr2.png)

After that, add the incoming mail server/port info, your username and password. Also, be sure you choose the SSL connection.

![Password ETC](http://imgur.com/UvKFB6H.png)

You will then be sent an email with a code that will verify the addition of this email account.

![Verification](http://imgur.com/zwVYBkB.png)

After that, you will see the additional email address in the **Accounts and Import** tab. I recommend selecting the “**Reply from the same address the message was sent to**” if you don’t want to worry about manually selecting the **From** field for each email you get. It’s a lot less mental overhead that way.

![Reply](http://imgur.com/QKPSOQx.png)

After that, you will see the additional address available in the From: field of your Gmail account. 

![New Address](http://imgur.com/xAUFbTF.png)

And that’s all she wrote.