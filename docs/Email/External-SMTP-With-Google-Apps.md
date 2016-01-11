In the spirit of [Documentation December at Reclaim Hosting](https://reclaimhosting.com/category/documentation-december/), I’m following up on a tutorial I wrote about [Sending Mail from a Forwarded Email Address through Gmail](http://bavatuesdays.com/sending-mail-from-a-forwarded-email-address-gmail/). I was having issues adding my jim@reclaimhosting.com email account to my Gmail account as a sender. I checked and double-checked my SMTP settings, but no luck. I kept recieving the error message “Authentication failed. Please check your username/password.” I was stuck in a weird authentication limbo, and according to [this forum thread](https://productforums.google.com/forum/#!msg/gmail/GyeMcHv1U-g/OC2v0YPf2T8J) I was not alone.

What was worse, none of their suggested solutions worked for me. I then went to the oracle [Tim Owens](http://timmmmyboy.com/) who noted Google requires the use of external SMTP servers for sending to additional addresses, and given we are using Google Apps servers for our Reclaim Hosting email accounts, they’re probably not be considered external. And if there is anything resembling a theme in my life these days, it is the following: Timmmmyboy was right!

I used the SMTP servers and credentials for our [Mandrill](https://www.mandrill.com/) email account and it worked perfectly, the credentials look something like the following.

SMTP Host: smtp.mandrillapp.com
Port: 587
Username: your@mandrill.email
Password: yourmandrillpassword