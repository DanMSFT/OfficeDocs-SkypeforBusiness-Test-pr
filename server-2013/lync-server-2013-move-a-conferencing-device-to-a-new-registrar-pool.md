---
title: 'Lync Server 2013: Move a conferencing device to a new Registrar pool'
TOCTitle: Move a conferencing device to a new Registrar pool
ms:assetid: 26e02ca3-e881-4f90-8bf0-b13649108100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994025(v=OCS.15)
ms:contentKeyID: 51803934
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Move a conferencing device to a new Registrar pool in Lync Server 2013

 


Move a conferencing device from one Registrar pool to another by using the **Move-CsMeetingRoom** cmdlet. This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.


> [!NOTE]
> For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="http://go.microsoft.com/fwlink/p/?linkid=255876">http://go.microsoft.com/fwlink/p/?linkId=255876</A>.




## Moving a Conferencing Device to a New Registrar Pool

  - To move a conferencing device, you must specify the identity of the room to be moved, and then set the Target parameter to the fully qualified domain name (FQDN) of the Registrar pool the device will be moved to. For example:
    
        Move-CsMeetingRoom -Target "atl-cs-001.litwareinc.com" -Identity "Room 14"

For details, see the Help topic for the [Move-CsMeetingRoom](https://technet.microsoft.com/en-us/library/jj204889\(v=ocs.15\)) cmdlet.

