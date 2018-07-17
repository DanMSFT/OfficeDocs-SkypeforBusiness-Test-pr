---
title: 'Lync Server 2013: New-CsWebServiceConfiguration for Address Book management'
TOCTitle: New-CsWebServiceConfiguration for Address Book management
ms:assetid: 49e4ecc5-aa3e-4dd4-a32c-b0dea3758fab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429703(v=OCS.15)
ms:contentKeyID: 48184067
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# New-CsWebServiceConfiguration for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the New-CsWebServiceConfiguration cmdlet locally: RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "New-CsWebServiceConfiguration"}

The cmdlet New-CsWebServiceConfiguration defines a new configuration for Web Services in your organization. The scope for the Web Services configuration can only be at the site or service level. It cannot create a new Web Services configuration at the global level. Specifically of interest to the Address Book is the EnableGroupExansion attribute. If set to True, the Web Services can respond to requests for group expansion.

For example:

    New-CsWebServiceConfiguration -Identity site:Redmond -EnableGroupExpansion $False -UseCertificateAuth $True

## See Also


[New-CsWebServiceConfiguration](https://technet.microsoft.com/en-us/library/gg398440\(v=ocs.15\))

