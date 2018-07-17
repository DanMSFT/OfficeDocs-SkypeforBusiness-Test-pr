---
title: 'Lync Server 2013: Supported server collocation for edge components'
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Supported server collocation for edge components in Lync Server 2013

 


The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers. The following servers provide functions needed for external user access and must be deployed as dedicated servers:

  - Edge Server

  - Director (Optional)

  - Reverse proxy


> [!IMPORTANT]
> The reverse proxy does not need to be dedicated to serving only Lync Server 2013. For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all. If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.


