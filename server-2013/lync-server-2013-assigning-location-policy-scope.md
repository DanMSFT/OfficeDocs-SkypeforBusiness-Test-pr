---
title: 'Lync Server 2013: Assigning location policy scope'
TOCTitle: Assigning location policy scope
ms:assetid: e4c66517-c593-4253-b900-7b4dd8bddf2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205360(v=OCS.15)
ms:contentKeyID: 48185734
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Assigning location policy scope in Lync Server 2013

 


As with other Lync Server policies, location policies can be assigned at multiple scope levels: global, site, and user. However, the scope of user-level location policies behaves a bit differently than with other Lync Server policies. Not only can per-user location policies be applied to endpoint objects (such as Users and Common Area Phone contact objects), they can also be applied to Lync Server network sites. Network sites are groupings of client subnets associated with a geographical location (but may not necessarily be all subnets in an entire central site or branch site). Any clients connected to the subnets in a network site automatically pick up the location policy assigned to that network site. In cases where a user-level location policy is assigned both to a user and to a network site, the network site-based location policy overrides any per-user policy setting.

Each network site has a location policy assigned to it, and each policy will have different PSTN Usages, Notification URIs, and Conference URIs values assigned to it.


> [!NOTE]
> The reason for this special policy scoping behavior is so that when a user homed on a pool at one office site visits another site and has to make an emergency call, the E9-1-1 call routing settings appropriate to that network site will apply no matter what pool or site the user is assigned to.


