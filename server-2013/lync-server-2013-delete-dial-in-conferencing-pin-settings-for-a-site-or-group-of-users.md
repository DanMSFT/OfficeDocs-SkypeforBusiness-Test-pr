﻿---
title: 'Lync Server 2013: Delete dial-in conferencing PIN settings for a site or group of users'
TOCTitle: Delete dial-in conferencing PIN settings for a site or group of users
ms:assetid: 15a9faee-d024-4c0e-b2a0-fe7e7dc00589
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520955(v=OCS.15)
ms:contentKeyID: 48183498
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Delete dial-in conferencing PIN settings for a site or group of users in Lync Server 2013

 


Follow these steps to delete a user-level or a site-level PIN policy.


> [!NOTE]
> You cannot delete the global PIN policy.



## To delete a user or site PIN policy

1.  From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.

2.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  In the left navigation bar, click **Conferencing**, and then click **PIN Policy**.

4.  On the **PIN Policy** page, in the search field, type all or part of the name of the policy you want to delete.

5.  In the list of policies, click the policy that you want, click **Edit**, and then click **Delete**.

6.  Click **OK**.

