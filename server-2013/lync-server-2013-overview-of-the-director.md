﻿---
title: 'Lync Server 2013: Overview of the Director'
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Overview of the Director in Lync Server 2013

 


A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts. You optionally can deploy a Director in the following two scenarios:

  - If you enable access by external users by deploying Edge Servers, you should also deploy a Director. In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers. When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users. It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks. If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.

  - If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance. In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.

