﻿---
title: 'Lync Server 2013: Configuring the Lync Server computers that will be monitored'
TOCTitle: Configuring the Lync Server computers that will be monitored
ms:assetid: 9f1b2b91-d5af-42ad-a27d-b0815f762ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205118(v=OCS.15)
ms:contentKeyID: 48184927
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Configuring the Lync Server computers that will be monitored in Lync Server 2013

 


Because Lync Server 2013 does not use the central discovery process used in Microsoft Lync Server 2010, each Lync Server 2013 computer that you want to monitor must be able to self-report its existence to the management server. To make this possible, you must install the Operations Manager agent files on each of the computers to be monitored. After the agent files have been installed, you must configure the computer to act as a System Center proxy. Note that these procedures should be carried out after you have installed and configured Lync Server on these computers.

