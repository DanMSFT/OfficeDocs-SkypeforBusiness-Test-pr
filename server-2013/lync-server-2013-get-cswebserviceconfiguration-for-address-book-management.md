---
title: 'Lync Server 2013: Get-CsWebServiceConfiguration for Address Book management'
TOCTitle: Get-CsWebServiceConfiguration for Address Book management
ms:assetid: 0b223733-5224-47d1-9b47-2109e6f135c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429692(v=OCS.15)
ms:contentKeyID: 48183372
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Get-CsWebServiceConfiguration for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsWebServiceConfiguration cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsWebServiceConfiguration"}

Get-CsWebServiceConfiguration returns information of the Web Services configuration currently in use in your organization. Of interest to the Address Book Services is the status of Distribution List Expansion function. If the attribute EnableGroupExpansion is True, your organization currently allows group expansion.

For example:

    Get-CsWebServiceConfiguration -Identity site:Redmond

## See Also


[Get-CsWebServiceConfiguration](https://technet.microsoft.com/en-us/library/gg425751\(v=ocs.15\))

