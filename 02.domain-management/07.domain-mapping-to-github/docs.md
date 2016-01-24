---
title: 'Domain Mapping to GitHub'
taxonomy:
    category:
        - docs
---
Over the last couple of weeks a number of requests have come in at Reclaim Hosting from folks who what to map their domain (or a subdomain) on another service. [I’ve been writing about domain mapping for years on the bava](http://bavatuesdays.com/?s=domain+mapping), and I never get tired of the magical idea of pointing your domain (or a subdomain) to another service in order to maintain your identity in relationship to a URL rather than a service.

Two sites I have done this for recently are [GitHub](https://github.com) and [Squarespace](https://squarespace.com), so I’ll document the process for these two. There are many more services you can map your domain  to including Tumblr, WordPress.com, Blogger, Wix, Google Sites, etc., but I’ll start with GitHub in this post, SquareSpace in the next, and then try and build out the rest over the next few weeks.

**But first a bit about A Records vs. CNAME Records**

When you are mapping aa domain on GitHub pages (or on any site really) an important concept you want to try and wrap your head around is the difference between A Records and CNAME Records. I’m getting closer to full comprehension, but a little help never hurts so I took the following definition from [DNS Simple](https://support.dnsimple.com/articles/differences-a-cname-records/):

The [A record](https://support.dnsimple.com/articles/a-record) points a name to a specific IP. For example, if you want blog.dnsimple.com to point to the server 185.31.17.133 you will configure

*blog.dnsimple.com. A 185.31.17.133*

The [CNAME record](https://support.dnsimple.com/articles/cname-record/) points a name to another name, instead of an IP. The CNAME source represents an alias for the target name and inherits its entire resolution chain. Let’s take our blog as example.

*blog.dnsimple.com. CNAME aetrion.github.io.*

To summarize, an A record points a name to an IP. CNAME record can point a name to another CNAME...

It’s good practice to point domains using CNAME Records when possible because IP addresses can change, and when they do an A Record will break because it is hardcoded. You might think of CNAME Records as relative hostnames, hence the IP address can change regularly but the mapped domain will not break.

One issue is that root domains (sometimes called “zone apex” or “naked domain”) have to be setup as an A Record, not a CNAME. This means that with most DNS providers you can setup a subdomain CNAME  (blog.jimgroom.me) to point to a service like GitHub, but you cannot setup your root domain (jimgroom.me) as a CNAME. That root domain would have to be an A Record. Make sense? Good.

**Mapping your Domain on GitHub**

As you might have guessed from the above definitions, there are two methods for mapping a custom domain on GitHub: CNAME and A Records. You can get a good overview of [how Custom Domains work on GitHub here](https://help.github.com/articles/about-custom-domains-for-github-pages-sites/). Mapping a subdomain using a CNAME is recommended so the domain doesn’t break if the server IP changes, which may very well happen. That said, we understand sometimes you just need that root domain mapped, so an A Record is nice and will suffice.

**Mapping your Root Domain with A Records**

For this example I’ll be mapping the root domain jimgroom.me onto a Github page. In terms of getting your Github pages setup for this see GitHub’s “Setting Up a Custom Domain with GitHub Pages.”

First you need to find the Advanced Zone Editor under the Domains section in CPanel.

![Advanced Zone Editor](http://i.imgur.com/SSXCSpg.png)

After that you need to choose the root domain you will be mapping. In the example screenshot below you’ll see I have several, but you may only have one which would be the default.

![Root Domain](http://i.imgur.com/VUYfRe7.png)

Once you select the domain you need to create two A Records for it using the below screenshot as a template, through the Name will obviously be different depending on the root domain you are mapping. The two a Records will point to the following IP addresses on GitHub: **192.30.252.153** and **192.30.252.154**.  You need to create a separate A Record for each of these IPs.

![A Records](http://imgur.com/LZWIJuc.png)

Once you have created both A Records in the Advanced DNS Zone Editor you should be all set. GitHub has their own documentation with [“Tips for Configuring an A Record with Your DNS Provider”](https://help.github.com/articles/tips-for-configuring-an-a-record-with-your-dns-provider/) that might also be useful. If you are having any issue see GitHub’s [“My Custom Domain Isn’t Working”](https://help.github.com/articles/my-custom-domain-isn-t-working/) or contact us.

**Mapping your Subdomain with CNAME Records**

For this example I’ll be mapping the subdomain [blog.jimgroom.com](https://help.github.com/articles/adding-a-cname-file-to-your-repository/) onto a GitHub Pages Repository using a CNAME Record. Head to Advanced DNS Settings.

![Zone Editor](http://i.imgur.com/SSXCSpg.png)

Once there, select the domain you will be mapping to if you have more than one.

![Mapping](http://imgur.com/gAWqTlJ.png)

Now you name to add a CNAME Record with the subdomain you are mapping in the Name field and the URL of your GitHub account in the CNAME field.

![CNAME](http://imgur.com/on42FOd.png)

After that you should be set. I found even if your repository is jimgroom.github.io/blog like mine is in this instance, you only need jimgroom.githib.io in the CNAME field.

GitHub provides a page with “Tips for configuring a CNAME record with your DNS provider” if you need more help, or feel free to contact us at Reclaim Hosting.

