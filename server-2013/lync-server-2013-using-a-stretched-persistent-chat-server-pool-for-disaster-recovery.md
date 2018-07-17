﻿---
title: 'Lync Server 2013: Using a stretched Persistent Chat Server pool for disaster recovery'
TOCTitle: Using a stretched Persistent Chat Server pool for disaster recovery
ms:assetid: 74c5287e-d70d-490a-9adc-ab419917ddd9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205007(v=OCS.15)
ms:contentKeyID: 48184506
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013

 


The disaster recovery solution for Persistent Chat Server is built on a stretched Persistent Chat Server pool. This is similar to metropolitan site resiliency in Lync Server 2010; however, there is no requirement for a stretched virtual local area network (VLAN). By stretching Persistent Chat Server pool, you essentially configure one pool in the topology logically, but you physically place the servers in the pool in two different data centers. Configure SQL Server mirroring for the database in the same way, and deploy the database and the mirror in the same data center. You need to configure a backup database in the secondary data center (with an optional mirror to provide high availability during disaster recovery). This is the backup database used for failover during disaster recovery.

For details about how to configure SQL Server mirroring for high availability, see [SQL Server mirroring in Lync Server 2013](lync-server-2013-sql-server-mirroring.md). For details about failing over the database for disaster recovery, see [Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md) and [Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013](lync-server-2013-setting-up-sql-server-log-shipping-between-the-primary-mirror-and-the-log-shipping-secondary-database.md).

