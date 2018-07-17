﻿---
title: 'Lync Server 2013: Viewing network subnet information'
TOCTitle: Viewing network subnet information
ms:assetid: 46f165f2-efe3-4cc1-9fee-a78b7f2ed41e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688044(v=OCS.15)
ms:contentKeyID: 49733636
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Viewing network subnet information in Lync Server 2013

 


You can use the following procedure to view a network subnet. From the Lync Server Control Panel, you can create, modify, or delete a network subnet. For details about creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).

## To view a network subnet

1.  From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.

2.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  In the left navigation bar, click **Network Configuration** and then click **Subnet**.

4.  On the **Subnet** page, click the subnet that you want to view.
    

    > [!NOTE]
    > You can only view one subnet at a time.



5.  On the **Edit** menu, click **Show details…**.

## Viewing Network Subnet Configuration Information by Using Windows PowerShell Cmdlets

Network subnet information can be viewed by using Windows PowerShell and the Get-CsNetworkSubnet cmdlet. This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell. For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [http://go.microsoft.com/fwlink/p/?linkId=255876](http://go.microsoft.com/fwlink/p/?linkid=255876).

## To view network subnet information

  - To view information about all your network subnets, type the following command in the Lync Server Management Shell and then press ENTER:
    
        Get-CsNetworkSubnet
    
    That will return information similar to this:
    
        Identity      : 172.11.15.0
        MaskBits      : 28
        Description   :
        NetworkSiteID : Redmond
        SubnetID      : 172.11.15.0

For more information, see the help topic for the [Get-CsNetworkSubnet](https://technet.microsoft.com/en-us/library/gg412825\(v=ocs.15\)) cmdlet.

## See Also


[Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md)  
[Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md)

