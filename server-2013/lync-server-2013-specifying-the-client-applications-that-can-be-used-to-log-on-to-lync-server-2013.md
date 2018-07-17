﻿---
title: 'Lync Server 2013: Specifying the client applications that can be used to log on to Lync Server 2013'
TOCTitle: Specifying the client applications that can be used to log on to Lync Server 2013
ms:assetid: d256a581-9a48-4d1a-82cc-2e1f520d7d2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182591(v=OCS.15)
ms:contentKeyID: 48185450
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Specifying the client applications that can be used to log on to Lync Server 2013

 


Lync Server 2013 enables you to specify the version of clients that are supported in your environment. Using client version policies can help reduce the costs associated with supporting multiple client versions. It can also improve the overall user experience, because when earlier and later versions of clients interact, the available features can be limited by the earlier version of the client.

There are three components of client version control:

  - Client version configuration settings are used to turn client version control on or off, either globally or for particular sites.

  - Client version policies are used to assign a set of rules globally, or to a particular site, pool, or group of users.

  - Client version policy rules make up a client version policy, and are used to define the actions that should be taken when users attempt to log on with specific clients and client versions.


> [!NOTE]
> Because anonymous users are not associated with a user, site, or service, anonymous users are affected by global-level policies only.



## In This Section

  - [Client version configuration settings in Lync Server 2013](lync-server-2013-client-version-configuration-settings.md)

  - [Client version policies in Lync Server 2013](lync-server-2013-client-version-policies.md)

  - [Client version rules in Lync Server 2013](lync-server-2013-client-version-rules.md)

## See Also


[Managing devices, phones, and client applications in Lync Server 2013](lync-server-2013-managing-devices-phones-and-client-applications.md)

