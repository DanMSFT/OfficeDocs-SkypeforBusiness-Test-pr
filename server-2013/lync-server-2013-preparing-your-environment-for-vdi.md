---
title: 'Lync Server 2013: Preparing your environment for VDI'
TOCTitle: Preparing your environment for VDI
ms:assetid: a3ec2e13-1a73-4b1c-a54a-8db7d4cd50f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205154(v=OCS.15)
ms:contentKeyID: 48185052
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Preparing your Lync Server 2013 environment for VDI

 


To prepare the environment for the Lync VDI plug-in, the administrator must perform the following steps.

1.  In Lync Server 2013, ensure that EnableMediaRedirection is set to TRUE for all VDI users. For details, see the Help topics for the [New-CsClientPolicy](https://technet.microsoft.com/en-us/library/gg425949\(v=ocs.15\)) cmdlet and the [Set-CsClientPolicy](https://technet.microsoft.com/en-us/library/gg398300\(v=ocs.15\)) cmdlet.

2.  On the data center computer, install the Lync 2013 client on all virtual machines.

3.  On the local computers, install the Lync VDI plug-in.

