﻿---
title: 'Lync Server 2013: Enable Quality of Experience'
TOCTitle: Enable Quality of Experience
ms:assetid: c8bb3c67-b324-4d94-8158-00c792c7ac42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182583(v=OCS.15)
ms:contentKeyID: 48185385
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Enable Quality of Experience in Lync Server 2013

 


Quality of Experience (QoE) records numeric data that indicates the media quality and information about participants, device names, drivers, IP addresses, and endpoint types involved in calls and sessions. For details, see [Planning for monitoring in Lync Server 2013](lync-server-2013-planning-for-monitoring.md) in the Planning documentation.

Use the following procedure to enable QoE for your whole organization or each site in your organization.


> [!NOTE]
> To enable QoE, you must first configure monitoring and a monitoring back-end database. For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.



## To enable QoE by using Lync Server Control Panel

1.  From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.

2.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.

4.  On the **Quality of Experience Data** page, click the appropriate collection from the table, click **Action**, and then click **Enable QoE**.

## Enabling QoE by Using Windows PowerShell Cmdlets

You can enable QoE by using Windows PowerShell and the **Set-CsQoEConfiguration** cmdlet. You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell. For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [http://go.microsoft.com/fwlink/p/?linkId=255876](http://go.microsoft.com/fwlink/p/?linkid=255876).

## To enable QoE for a single location

  - To enable QoE, set the EnableQoE parameter to True ($True).
    
        Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $True

## To disable QoE for a single location

  - To disable QoE, set the EnableQoE parameter to False ($False). This does not uninstall monitoring. It pauses the collection and storage of QoE data.
    
        Set-CsQoEConfiguration -Identity "site:Redmond" -EnableQoE $False

## To use a single command to enable QoE in multiple locations

  - This command enables QoE for all the QoE configuration settings currently in use in your organization.
    
        Get-CsQoEConfiguration | Set-CsQoEConfiguration "site:Redmond" -EnableQoE $True

For details, see [Set-CsQoEConfiguration](https://technet.microsoft.com/en-us/library/gg398245\(v=ocs.15\)).

## See Also


[Planning for monitoring in Lync Server 2013](lync-server-2013-planning-for-monitoring.md)  
[Deploying monitoring in Lync Server 2013](lync-server-2013-deploying-monitoring.md)

