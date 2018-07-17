---
title: 'Lync Server 2013: Set-CsAddressBookConfiguration for Address Book management'
TOCTitle: Set-CsAddressBookConfiguration for Address Book management
ms:assetid: 3a64ceb1-9f79-4f3b-bf33-eaf346dbd60d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429700(v=OCS.15)
ms:contentKeyID: 48183913
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Set-CsAddressBookConfiguration for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsAddressBookConfiguration"}

Set-CsAddressBookConfiguration is similar to the New-CsAddressBookConfiguration cmdlet, except it is used to modify an existing configuration.

For example:

    Set-CsAddressBookConfiguration -identity site:Redmond -RunTimeOfDay 23:00

## See Also


[Set-CsAddressBookConfiguration](https://technet.microsoft.com/en-us/library/gg412784\(v=ocs.15\))

