---
title: 'Lync Server 2013: Viewing location policy information'
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Viewing location policy information in Lync Server 2013

 


In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts. The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call. For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.

You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel. From Lync Server Control Panel you can view, create, modify, or delete location policies. Use the following procedure to view information about location policies. For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).

## To view information about a location policy

1.  From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.

2.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  In the left navigation bar, click **Network Configuration** and then click **Location Policy**.

4.  On the **Location Policy** page, select the location policy that you want to modify.

5.  On the **Edit** menu, click **Show details**.
    

    > [!NOTE]
    > You can only view information about one location policy at a time.



A single policy, called Global, exists by default and cannot be deleted or renamed. However, you can modify the Global policy. This policy will apply to all users and contacts, unless you create site policies or per-user policies. Per-user policies must be applied to specific users.

## See Also


[Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md)  
[Create or modify a network site in Lync Server 2013](lync-server-2013-create-or-modify-a-network-site.md)  


[New-CsLocationPolicy](https://technet.microsoft.com/en-us/library/gg398231\(v=ocs.15\))  
[Set-CsLocationPolicy](https://technet.microsoft.com/en-us/library/gg412987\(v=ocs.15\))  
[Remove-CsLocationPolicy](https://technet.microsoft.com/en-us/library/gg398727\(v=ocs.15\))  
[Get-CsLocationPolicy](https://technet.microsoft.com/en-us/library/gg398911\(v=ocs.15\))

