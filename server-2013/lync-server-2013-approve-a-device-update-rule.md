﻿---
title: 'Lync Server 2013: Approve a Device Update rule'
TOCTitle: Approve a Device Update rule
ms:assetid: 9dbb1c9a-be0f-4e13-9234-05501ab43ac5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994053(v=OCS.15)
ms:contentKeyID: 51803964
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Approve a Device Update rule in Lync Server 2013

 


After you import a device update rule, it’s installed on your test devices. If your testing is successful, and you want to roll out the update to your organization, approve it by using either Lync Server Control Panel or Windows PowerShell.

## To approve a device update rule by using Lync Server Control Panel

1.  From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.

2.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  On the **Device Update** page, do one of the following:
    
      - To approve one rule, select that rule.
    
      - To approve all rules, click **Edit**, and then click **Select All**.

4.  Click **Action**, and then click **Approve**.

## Approving a Device Update Rule by Using Windows PowerShell Cmdlets

Device update rules can also be approved by using Windows PowerShell and the **Approve-CsDeviceUpdateRule** cmdlet. This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.


> [!NOTE]
> For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="http://go.microsoft.com/fwlink/p/?linkid=255876">http://go.microsoft.com/fwlink/p/?linkId=255876</A>.



## To approve a single device update rule

  - The following command approves the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 found on the Web server atl-cs-001.litwareinc.com:
    
        Approve-CsDeviceUpdateRule -Identity service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9

## To approve multiple device update rules

  - This command approves all the device update rules for Microsoft-branded devices:
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Approve-CsDeviceUpdateRule

For details, see the Help topic for the [Approve-CsDeviceUpdateRule](https://technet.microsoft.com/en-us/library/gg398949\(v=ocs.15\)) cmdlet.

## See Also


[Import Device Update rules in Lync Server 2013](lync-server-2013-import-device-update-rules.md)  
[Restore a Device Update rule in Lync Server 2013](lync-server-2013-restore-a-device-update-rule.md)

