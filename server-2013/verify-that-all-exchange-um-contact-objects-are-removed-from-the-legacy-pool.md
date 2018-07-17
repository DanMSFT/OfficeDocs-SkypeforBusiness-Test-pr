---
title: Verify that all Exchange UM Contact objects are removed from the legacy pool
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Verify that all Exchange UM Contact objects are removed from the legacy pool

 


Use either the **OCSUmUtil** tool or the **Get-CsExumContact** cmdlet to verify that Exchange UM contact objects have been removed from the legacy Office Communications Server 2007 R2 pool. **OCSUmUtil** is located in the following folder:

%Program Files%\\Common Files\\Lync Server 2013\\Support\\OcsUMUtil.exe

**OCSUmUtil** must be run from a user account that has:

  - Membership in the RTCUniversalServerAdmins and RTCUniversalUserAdmins group (which includes rights to read Exchange Server Unified Messaging settings)

  - Domain rights to create contact objects in the specified organizational unit (OU) container

For details about using the **Get-CsExumContact** cmdlet, see [Get-CsExUmContact](https://technet.microsoft.com/en-us/library/gg412725\(v=ocs.15\)) in the Lync Server Management Shell documentation.

