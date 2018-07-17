---
title: 'Lync Server 2013: Set-CsWebServiceConfiguration for Address Book management'
TOCTitle: Set-CsWebServiceConfiguration for Address Book management
ms:assetid: 79d0edf5-23f3-4845-a7b7-e11b5a928bab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429709(v=OCS.15)
ms:contentKeyID: 48184572
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Set-CsWebServiceConfiguration for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the Set-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Set-CsWebServiceConfiguration"}

The Set-CsWebServiceConfiguration cmdlet allows the administrator to redefine an existing attribute in the configuration of the Web Services.

For example:

    Set-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $True

## See Also


[Set-CsWebServiceConfiguration](https://technet.microsoft.com/en-us/library/gg398396\(v=ocs.15\))

