﻿---
title: 'Lync Server 2013: Verify access through your reverse proxy'
TOCTitle: Verify access through your reverse proxy
ms:assetid: 3076a786-e022-4d41-91ec-1bf252b2a468
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429697(v=OCS.15)
ms:contentKeyID: 48183753
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Verify access through your reverse proxy in Lync Server 2013

 


Use the following procedure to verify that your users can access information on the reverse proxy. You might need to complete the firewall configuration and Domain Name System (DNS) configuration before access will work correctly.

## To verify that you can access the website through the Internet

  - Open a web browser, type the URLs in the **Address** bar that clients use to access the Address Book files and the website for conferencing as follows:
    
      - For Address Book Server, type a URL similar to the following: **https://externalwebfarmFQDN/abs** where externalwebfarmFQDN is the external FQDN of the external web services that hosts Address Book services. The user should receive an HTTP challenge, because directory security on the Address Book Server folder is configured to Windows authentication by default.
    
      - For conferencing, type a URL similar to the following: **https://externalwebfarmFQDN/meet** where externalwebfarmFQDN is the external FQDN of the web farm that hosts meeting content. This URL should display the troubleshooting page for conferencing. Alternatively, confirm that your Simple URL for conferencing functions correctly. An example Simple URL for the conference join might be https://meet.contoso.com
    
      - For distribution group expansion, type a URL similar to the following: **https://externalwebfarmFQDN/GroupExpansion/service.svc**. The user should receive an HTTP challenge, because directory security on the distribution group expansion service is configured to Windows authentication by default.
    
      - For dial-in, type the simple URL similar to the following **https://externalwebfarmFQDN/dialin** where externalwebfarmFQDN is the external FQDN of the web farm that hosts the dial-in page for dial-in conferencing. The user should be directed to the dial-in page. Alternatively, confirm that your Simple URL dial-in functions correctly. An example Simple URL for dial-in might be https://dialin.contoso.com
    
      - To confirm that the autodiscover URL is working, type https://lyncdiscover. externaldomainFQDN. The browser should prompt you to open a file. Select Notepad to open it. A typical response would be similar to:
        
            {"AccessLocation":"External","Root":{"Links":[{"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/domain","token":"Domain"},
            {"href":"https:\/\/extweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/user","token":"User"},
            {"href":"https:\/\/lyncweb.contoso.com\/Autodiscover\/AutodiscoverService.svc\/root\/oauth\/user","token":"OAuth"}]}}

