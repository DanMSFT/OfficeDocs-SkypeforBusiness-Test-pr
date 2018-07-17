---
title: 'Lync Server 2013: Set up certificates for the reverse proxy'
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Set up certificates for the reverse proxy in Lync Server 2013

 


Each reverse proxy server requires a web server certificate for use by the listening service. The web server certificate must be issued by a public certification authority (CA).

For details about this and other certificate requirements, see [Certificate requirements for external user access in Lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).

## To set up a Web Services certificate for the reverse proxy

  - You should have already set up your reverse proxy, including setting up the Web Services certificate. If you did not do so before starting your deployment of your Edge Servers, use the procedures in [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) to create request and install the Web Services certificate, and then create each web publishing rule and configure it to use the certificate.

