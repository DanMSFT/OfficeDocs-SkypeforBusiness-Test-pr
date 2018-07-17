---
title: Remove a Front End Server from a pool
TOCTitle: Remove a Front End Server from a pool
ms:assetid: 767225c9-7c0b-4d54-a407-d77134ba2abe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688095(v=OCS.15)
ms:contentKeyID: 49733694
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Remove a Front End Server from a pool

 


The Microsoft Lync Server 2010 Enterprise Edition Front End Server cannot exist as a stand-alone computer. It must be defined as a Front End pool, even if there is only a single computer in the pool.

This topic guides you through the process of removing an individual Front End Server from an existing Front End pool. If the Front End Server is the last server in the pool or if you are removing the pool completely, see [Remove Front End pool or Standard Edition server](remove-front-end-pool-or-standard-edition-server.md). There is no need to remove the individual Front End Servers before you remove the Front End pool. When you remove the pool, you remove each Front End Server.

## To remove a Front End Server from a pool

1.  Open the Lync Server 2013 Front End Server, open Topology Builder.

2.  Navigate to the Lync Server 2010 node.

3.  Expand **Enterprise Edition Front End pools**, expand the Front End pool with the Front End Server that you want to remove, right-click the Front End Server that you want to remove, and then click **Delete**.

