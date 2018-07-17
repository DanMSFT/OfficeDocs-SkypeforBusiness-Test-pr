﻿---
title: 'Lync Server 2013: Technical requirements for media bypass'
TOCTitle: Technical requirements for media bypass
ms:assetid: 6162a204-0e7c-460a-8eb2-e592c6590a8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398435(v=OCS.15)
ms:contentKeyID: 48184321
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Technical requirements for media bypass in Lync Server 2013

 


For each call to the PSTN, the Mediation Server determines whether media from the Lync endpoint of origin can be sent directly to a Mediation Server peer without traversing the Mediation Server. The peer can be a PSTN gateway, IP-PBX, or Session Border Controller (SBC) at an Internet telephony service provider (ITSP) that is associated with the trunk between the Mediation Server where the call is routed.

Media bypass can be employed when the following requirements are met:

  - A Mediation Server peer must support the necessary capabilities for media bypass, the most important being the ability to handle multiple forked responses (known as “early dialogs”). Contact the manufacturer of your gateway or PBX, or your ITSP, to obtain the value for the maximum number of early dialogs that the gateway, PBX, or SBC can accept.

  - The Mediation Server peer must accept media traffic directly from Lync endpoints. Many ITSPs allow their SBC to receive traffic only from the Mediation Server. Contact your ITSP to determine whether its SBC accepts media traffic directly from Lync endpoints.

  - Lync clients and a Mediation Server peer must be well connected, meaning that they are either located in the same network region or at network sites that connect to the region over WAN links that have no bandwidth constraints

## See Also


[Media bypass modes in Lync Server 2013](lync-server-2013-media-bypass-modes.md)  
[Media bypass and call admission control in Lync Server 2013](lync-server-2013-media-bypass-and-call-admission-control.md)

