---
title: 'Lync Server 2013: Changing the Edge pool associated with a Front End pool'
TOCTitle: Changing the Edge pool associated with a Front End pool
ms:assetid: 369468c7-2c0b-48cc-bbc3-825dad7b85aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688023(v=OCS.15)
ms:contentKeyID: 49733613
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Changing the Edge pool associated with a Front End pool in Lync Server 2013

 


If an Edge pool goes down but the Front End pool at the same site is still running, you will need to set the Front End pool to use an Edge pool at a different site until the failed Edge pool is restored.

## Changing the Edge Pool Associated with a Front End Pool

1.  In Topology Builder, navigate to the name of the Front End pool you need to change.

2.  Right-click the pool, and then click **Edit Properties**.

3.  In the **Associations** section, under **Associate Edge Pool (for media components)**, use the drop down box to select the Edge pool you want to associate this Front End pool with.

4.  Click **OK**.

## See Also


[Edge Server disaster recovery in Lync Server 2013](lync-server-2013-edge-server-disaster-recovery.md)

