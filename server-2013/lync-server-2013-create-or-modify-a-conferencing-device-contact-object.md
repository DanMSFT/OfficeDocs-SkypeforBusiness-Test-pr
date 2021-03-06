﻿---
title: 'Lync Server 2013: Create or modify a conferencing device Contact object'
TOCTitle: Create or modify a conferencing device Contact object
ms:assetid: 62ed64be-379c-417d-9453-511881cf5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994035(v=OCS.15)
ms:contentKeyID: 51803945
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Create or modify a conferencing device Contact object in Lync Server 2013

 


To create a conferencing room object, first create an Active Directory user account to represent the device. Then, use the **Enable-CsMeetingRoom** cmdlet to enable that account to function as a conferencing device. If you need to change the properties of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet.

These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.


> [!NOTE]
> For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="http://go.microsoft.com/fwlink/p/?linkid=255876">http://go.microsoft.com/fwlink/p/?linkId=255876</A>.




## Creating a Conferencing Device

  - After you create the Active Directory user account that represents the new conferencing device, enable it by using the **Enable-CsMeetingRoom** cmdlet. Be sure to include a) the conferencing device identity, b) the registrar pool where the room account will be homed, and c) the SIP address to be assigned to that account. For example:
    
        Enable-CsMeetingRoom -Identity "Redmond Conferencing device" -RegistrarPool "atl-cs-001.litwareinc.com" -SipAddress "sip:RedmondMeetingRoom@litwareinc.com"

## Modifying a Conferencing Device

  - To modify the property values of an existing conferencing device, use the **Set-CsMeetingRoom** cmdlet. For example, the following command updates the phone number (LineUri) associated with a conferencing device:
    
        Set-CsMeetingRoom -Identity "Redmond Conferencing device" -LineUri "tel:+12065551219"

For details, see the Help topics for the [Enable-CsMeetingRoom](https://technet.microsoft.com/en-us/library/jj205062\(v=ocs.15\)) cmdlet and the [Set-CsMeetingRoom](https://technet.microsoft.com/en-us/library/jj204831\(v=ocs.15\)) cmdlet.

