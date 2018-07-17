---
title: 'Lync Server 2013: Import Device Update rules'
TOCTitle: Import Device Update rules
ms:assetid: 919e9c87-912b-4bc9-92e7-5998fc2e0bf0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994056(v=OCS.15)
ms:contentKeyID: 51803967
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Import Device Update rules in Lync Server 2013

 


Device update rules can be imported only by using Windows PowerShell and the **Import-CsDeviceUpdate** cmdlet. This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.


> [!NOTE]
> For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="http://go.microsoft.com/fwlink/p/?linkid=255876">http://go.microsoft.com/fwlink/p/?linkId=255876</A>.




## To import device update rules to a single web server

  - The following command imports device update rules to the Web server atl-cs-001.litwareinc.com:
    
        Import-CsDeviceUpdate -Identity "service:WebServer:atl-cs-001.litwareinc.com" -FileName C:\Updates\UCUpdates.cab

## To import device update rules to all your web servers

  - In this example, device update rules are imported to all the Web servers deployed in your organization. For this command to work, the folder \\\\atl-fs-001.litwareinc.com\\Updates must be shared and available to all the Web servers.
    
        Get-CsService -WebServer | ForEach-Object {Import-CsDeviceUpdate -Identity $_.Identity -FileName \\atl-fs-001.litwareinc.com\Updates\UCUpdates.cab}

For details, see the Help topic for the [Import-CsDeviceUpdate](https://technet.microsoft.com/en-us/library/gg398861\(v=ocs.15\)) cmdlet.

## See Also


[View information about Device Update rules in Lync Server 2013](lync-server-2013-view-information-about-device-update-rules.md)  
[Approve a Device Update rule in Lync Server 2013](lync-server-2013-approve-a-device-update-rule.md)

