If you wish to use your domain name with a third-party service, it will often require you to edit your DNS to add an A record or CNAME Record. Here's how to do that within the Reclaim Hosting control panel.

Login to your control panel and navigate to the **Advanced Zone Editor**

![image](http://i.imgur.com/pIUqgLp.png)

If you have more than one domain you will need to select which domain name you will be mapping from the dropdown menu. If you only have one domain it will automatically be selected.

![image](http://i.imgur.com/jfzkjcd.png)

If the service provider you are mapping the domain to provides an IP Address and instructs you to map an A record, click **Edit** next to the A record for that domain. If you are mapping a subdomain you will find a separate A record for the subdomain.

![image](http://i.imgur.com/Pku0eSu.png)

Replace your server's IP address with the IP address provided by the third-party service and click **Edit Record** to save the changes. DNS changes can take up to **24 hours** to propagate globally.

![image](http://i.imgur.com/eMuVOnC.png)

If the service you are mapping a domain to provides a **CNAME** the process is very similar. Find the CNAME record for the domain, which will be prefixed with www. and edit the record to point to the domain name that the service provides to you. CNAME records require either the domain be a subdomain or have the www. prefix.