---
title: 'Lync Server 2013: Test-CsAddressBookWebQuery for Address Book management'
TOCTitle: Test-CsAddressBookWebQuery for Address Book management
ms:assetid: 977a9c1f-5f4e-4539-9a26-8748b61a57d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429716(v=OCS.15)
ms:contentKeyID: 48184865
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Test-CsAddressBookWebQuery for Address Book management in Lync Server 2013

 


Who can run this cmdlet: By default, members of the following groups are authorized to run the Test-CsAddressBookWebQuery cmdlet: RTCUniversalServerAdmins. To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Test-CsAddressBookService"}

Similar to the Test-CsAddressBookService synthetic transaction, Test-CsAddressBookWebQuery performs a query against the Address Book Web Query to ensure that it is operating properly. The cmdlet will connect to the Web Ticket authentication and present the credentials specified in –UserCredential. If authenticated, the cmdlet then present the –TargetSipAddress information. The cmdlet should report success if it was able to retrieve the information about the contact.

For example:

    Test-CsAddressBookWebQuery -TargetFqdn atl-cs-001.contoso.com -UserCredential contoso\bob -UserSipAddress "sip:bob@contoso.com" -TargetSipAddress "sip:bob@contoso.com"

## See Also


[Test-CsAddressBookWebQuery](https://technet.microsoft.com/en-us/library/gg398773\(v=ocs.15\))

