---
title: 'Installing Free SSL Certificates'
published: true
visible: true
taxonomy:
    category:
	- docs
---

Reclaim Hosting provides **free** SSL certificates through the [Let's Encrypt](https://letsencrypt.org/) project for all users. To get started navigate to your cPanel account and click the Let's Encrypt icon located under the **Security** section.

![Let's Encrypt Icon](Screen%20Shot%202016-01-28%20at%2011.39.28%20PM.png)

The interface will list all of your domains with those secured with a Let's Encrypt certificate at the top. To install a new certificate to a domain click the **Issue** button next to the domain.

![Let's Encrypt List Domains](Screen%20Shot%202016-01-28%20at%2011.56.55%20PM.png)

You will be given an option to provision the certificate to the main domain as well as subdomains including www. Check the box next to any domains that should be secured with the certificate (NOTE: Let's Encrypt does not currently issue wildcard subdomain certificates)

![Select Domains](Screen%20Shot%202016-01-28%20at%2011.57.26%20PM.png)

Once you're ready to go, click the **Issue** button at the bottom of the page. If successful, the domain will be secured with a free TLS SSL certificate provided by Let's Encrypt.

![Certificate Installed Successfully](Screen%20Shot%202016-01-28%20at%2011.58.03%20PM.png)

###Troubleshooting

**The Let's Encrypt HTTP Challenge Failed** - This error can occur if the domain you are attempting to install an SSL certificate is not currently hosted with us. Let's Encrypt attempts to verify domain records by reading a file placed in the root directory of the domain. If the domain is not resolving to our servers this test will fail.
