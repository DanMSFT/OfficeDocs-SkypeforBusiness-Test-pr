﻿---
title: 'Lync Server 2013: Viewing network interface information'
TOCTitle: Viewing network interface information
ms:assetid: e7dbb1ec-62b3-48be-a419-c493df5740e6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721916(v=OCS.15)
ms:contentKeyID: 49733850
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Viewing network interface information in Lync Server 2013

 


You can view network interface information by using Windows PowerShell and the **Get-CsNetworkInterface** cmdlet. You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell. For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [http://go.microsoft.com/fwlink/p/?linkId=255876](http://go.microsoft.com/fwlink/p/?linkid=255876).

## To view network interface information

  - To view network interface information, type the following command in the Lync Server Management Shell and then press ENTER:
    
        Get-CsNetworkInterface
    
    This command returns information similar to the following for each network interface:
    
        Identity              : dc.vdomain.com/Primary/1
        ComputerFqdn          : dc.vdomain.com
        IPAddress             : 0.0.0.0
        IPv6Address           :
        Interface             : Primary
        InterfaceNumber       : 1
        ConfiguredFqdn        :
        ConfiguredIPAddress   :
        ConfiguredIPv6Address :
    
    For details, see [Get-CsNetworkInterface](https://technet.microsoft.com/en-us/library/gg398121\(v=ocs.15\)).

