﻿---
title: 'Lync Server 2013: Update-CsAddressBook for Address Book management'
TOCTitle: Update-CsAddressBook for Address Book management
ms:assetid: 0ffd2ef8-201c-44aa-8c64-1c7b0eaa7d48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429695(v=OCS.15)
ms:contentKeyID: 48183428
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Update-CsAddressBook for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the Update-CsAddressBook cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Update-CsAddressBook"}

The Update-CsAddressBook cmdlet replaces the **abserver.exe –syncNow** command from Office Communications Server. The cmdlet’s purpose is to initiate a synchronization immediately rather than waiting for the scheduled time. The first example command updates all Address Books in the organization. The second updates only the Address Book associated with the defined server.


> [!NOTE]
> In Lync Server 2013, Lync Server User Replicator will pick up the changes from Active Directory and update the Lync Server user database based on a configured interval. Lync Server User Replicator will also propagate the changes to the RTCab database quickly without the administrator having to run Update-CSAddressBook. Administrators will only need to run Update -CSAddressBook if the Address Book file download is enabled.



For example:

    Update-CsAddressBook

    Update-CsAddressBook -Fqdn atl-abs-001.contoso.com

## See Also


[Update-CsAddressBook](https://technet.microsoft.com/en-us/library/gg398194\(v=ocs.15\))

