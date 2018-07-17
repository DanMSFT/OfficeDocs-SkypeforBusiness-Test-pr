﻿---
title: 'Phase 10: Decommission legacy site'
TOCTitle: 'Phase 10: Decommission legacy site'
ms:assetid: d591a310-3b5c-4092-b19e-0349616e40df
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205300(v=OCS.15)
ms:contentKeyID: 48185540
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Phase 10: Decommission legacy site

 


The following topics provide guidance in decommissioning pools, and deactivating and removing servers and pools from a legacy deployment of Office Communications Server 2007 R2. Not all of the procedures listed in this section are required. Read the information in each of these topics to determine which decommissioning procedure to use.


> [!WARNING]
> If you imported conference directories for dial-in conferencing to Lync Server 2013, it is important to transition conference directory ownership to Lync Server 2013 before you begin to decommission your pools. If you decommission a pool without first transitioning conference directory ownership, the dial-in feature for all migrated meetings will no longer work. You must perform the step to transition ownership once for each conference directory in your legacy pool.




> [!IMPORTANT]
> For information on migrating and upgrading Microsoft Unified Communications Managed API (UCMA) applications, prior to decommissioning your legacy environment, see <A href="http://go.microsoft.com/fwlink/p/?linkid=269555">http://go.microsoft.com/fwlink/p/?LinkId=269555</A>



## In This Section

  - [Move conference directories](move-conference-directories.md)

  - [Update DNS SRV records](update-dns-srv-records_1.md)

  - [Decommissioning servers and pools](decommissioning-servers-and-pools.md)

  - [Remove BackCompatSite](remove-backcompatsite.md)

