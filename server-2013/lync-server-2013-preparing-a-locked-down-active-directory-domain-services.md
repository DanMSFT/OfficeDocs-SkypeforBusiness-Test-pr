---
title: 'Lync Server 2013: Preparing a locked-down Active Directory Domain Services'
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Preparing a locked-down Active Directory Domain Services in Lync Server 2013

 


Organizations often lock down Active Directory Domain Services to help mitigate security risks. However, a locked-down Active Directory environment can limit the permissions that Lync Server 2013 requires. Properly preparing a locked-down Active Directory environment for Lync Server 2013 involves some additional considerations and steps.

Two common ways in which permissions are limited in a locked-down Active Directory environment are as follows:

  - Authenticated user access control entries (ACEs) are removed from containers.

  - Permissions inheritance is disabled on containers of User, Contact, InetOrgPerson, or Computer objects.

## In This Section

  - [Authenticated user permissions are removed in Lync Server 2013](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

