﻿---
title: 'Lync Server 2013: Delegation'
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Delegation in Lync Server 2013

 


The delegation capabilities in Lync are affected by Location-Based Routing in the following manner:

  - When a delegate enabled for Location-Based Routing places a call on behalf of a manager, the delegate’s voice policy is used to authorize the call and the delegate’s site voice routing policy will be used to route the call

  - For incoming PSTN calls to a manager, the same rules applicable for call forwarding or simultaneously ringing will apply as described in the Call transfers and forwarding and Simultaneous ringing topics.

  - When a delegate sets a PSTN endpoint as a simultaneous ring target, for an incoming call to the manager, the voice routing policy of the site that is associated to the incoming trunk will be used to route the call to the delegate’s PSTN endpoint.

  - For delegation, it’s recommended that the manager and his associated delegates to be usually located in the same network site.

## See Also


[Scenarios for Location-Based Routing in Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)

