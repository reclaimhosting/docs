---
title: 'Domain Mapping to Squarespace'
taxonomy:
    category:
        - docs
---
Building on the domain mapping documentation I am putting together for Reclaim Hosting (my last post took you through Domain Mapping on GitHub), this post will take you through how to point your domain to [Squarespace](https://squarespace.com). After you connect your domain over at Squarespace [(they provide a good tutorial for that process)](https://support.squarespace.com/hc/en-us/articles/205812378-Connecting-a-domain-to-your-Squarespace-site), a new panel will open providing you the records you need to enter into the Advanced DNS Editor at Reclaim Hosting so your domain can be pointed correctly to Squarespace.

![Domain Point](http://imgur.com/95Ciw3s.png)

For Squrespace you need to create two CNAME Records and four A Records. The CNAME records appear to be used as a way to verify your account. You can see an example of the two I created below. Keep in mind the Name field for the verify.squarespace.com CNAME will be have a unique code in front of your domain. What I have listed below for the Name field will be a value Squarespace will provide.

![Verify Squarespace](http://imgur.com/eX1xdnb.png)

The second CNAME you create will have www.yourdomain.com in your Name field.

![CNAME](http://imgur.com/9uLLdXs.png)

You will then need to add four A Records pointing to four different IP address that Squarespace provides you.

![Squarespace A Records](http://imgur.com/JS4FhEx.png)

Below is a look at the four A Records I created for this domain.

![4 Records](http://imgur.com/2EqAthY.png)

That should be all you need to get your domain mapped to Squarespace. I have never seen a service use both CNAME and A Records (not to mention 6 all told) for one domain, I imagine  they are building in a lot of redundancy, which is not necessarily a bad thing, just a bit more work at the point of setup.