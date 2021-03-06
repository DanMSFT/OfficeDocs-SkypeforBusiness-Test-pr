﻿---
title: 'Lync Server 2013: Disable a user for Enterprise Voice'
TOCTitle: Disable a user for Enterprise Voice
ms:assetid: 462002d8-21df-4d77-bf7f-4d059d6a4bb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688043(v=OCS.15)
ms:contentKeyID: 49733635
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Disable a user for Enterprise Voice in Lync Server 2013

 


Use the following procedure to disable Enterprise Voice for a user account that is enabled for Lync Server 2013.

## To disable a user account for Enterprise Voice

1.  From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.

2.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  In the left navigation bar, click **Users**.

4.  In the **Search users** box, type all or the first portion of the display name, first name, last name, Security Accounts Manager (SAM) account name, SIP address, or line Uniform Resource Identifier (URI) of the user account that you want to enable, and then click **Find**.

5.  In the table, click the user account that you want to enable for Enterprise Voice.

6.  On the **Edit** menu, click **Show details**.

7.  On the **Edit Lync Server User** page, under **Telephony**, click any option except **Enterprise Voice**.
    

    > [!NOTE]
    > To restrict a user from making audio or video calls by using Lync, under <STRONG>Telephony</STRONG>, click <STRONG>Audio/video disabled</STRONG>.



8.  Click **Commit**.

The user is now unable to use the Enterprise Voice feature.

## See Also


[Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md)  


[Managing Enterprise Voice for users in Lync Server 2013](lync-server-2013-managing-enterprise-voice-for-users.md)  
[Lync Server 2013 Management Shell](https://technet.microsoft.com/en-us/library/gg398474\(v=ocs.15\))

