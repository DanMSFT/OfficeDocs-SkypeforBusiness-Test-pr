---
title: 'Lync Server 2013: Remove-CsAddressBookConfiguration for Address Book management'
TOCTitle: Remove-CsAddressBookConfiguration for Address Book management
ms:assetid: 5d173ebe-ec4d-4640-8432-a25071ea9cc5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429705(v=OCS.15)
ms:contentKeyID: 48184258
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Remove-CsAddressBookConfiguration for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the Remove-CsAddressBookConfiguration cmdlet locally: RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsAddressBookConfiguration"}

As the name implies, Remove-CsAddressBookConfiguration will remove the configuration based on the defined Site Identity.

For example:

    Remove-CsAddressBookConfiguration -Identity site:Redmond

## See Also


[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/en-us/library/gg398934\(v=ocs.15\))

