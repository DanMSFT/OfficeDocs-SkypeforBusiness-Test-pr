---
title: 'Lync Server 2013: Clients supported for Response Group'
TOCTitle: Clients supported for Response Group
ms:assetid: 84911025-e754-41a8-ba48-e31c058fc557
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398674(v=OCS.15)
ms:contentKeyID: 48184705
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Clients supported for Response Group in Lync Server 2013

 


The Response Group application supports the following clients:

  - Lync 2013 desktop client

  - Lync 2010 desktop client

  - Lync 2010 Attendant

  - Office Communications Server 2007 R2 Attendant

  - Lync Phone Edition


> [!NOTE]
> The Response Group application is not supported on Lync mobile clients.



For details about new features, see [New Response Group application features in Lync Server 2013](lync-server-2013-new-response-group-application-features.md) in the Getting Started documentation.

The specific client that you can use depends on the type of Response Group user that you are:

  - **Callers** can call a response group by using any of the clients listed previously, and by using a standard telephone over the public switched telephone network (PSTN).

  - **Informal agents** (agents who do not sign into and out of their groups to accept calls) can accept calls by using Attendant, Lync, or Lync Phone Edition. Informal agents are automatically signed into their groups when they sign in to Lync Server 2013 by using one of these clients.

  - **Formal agents** (agents who must sign into and out of their groups to accept calls) can accept calls by using Lync 2013 and accessing the agent console from the menu item, or by using Attendant and accessing the agent console directly from Internet Explorer.

