---
title: 'Lync Server 2013: Using Topology Builder to configure high availability and disaster recovery'
TOCTitle: Using Topology Builder to configure high availability and disaster recovery
ms:assetid: abc1a25d-1f5e-46ef-91d2-0144fc847206
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205172(v=OCS.15)
ms:contentKeyID: 48185113
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013

 


Perform the following steps within Topology Builder to configure high availability and disaster recovery for Persistent Chat Server.

1.  Add the mirror databases and the log shipping secondary database SQL Server stores.

2.  Edit the Persistent Chat Server service properties to:
    
    1.  Enable mirroring for the primary database.
    
    2.  Add the primary mirror SQL Server store.
    
    3.  Enable the SQL Server Log Shipping database.
    
    4.  Add the SQL Server Log Shipping secondary SQL Server store.
    
    5.  Add the SQL Server store mirror for the secondary database.
    
    6.  Publish the topology.

