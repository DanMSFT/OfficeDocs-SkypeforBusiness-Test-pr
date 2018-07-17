---
title: 'Lync Server 2013: Backing up file stores'
TOCTitle: Backing up file stores
ms:assetid: 1a7f4e93-aa3d-461e-878e-2c572baa1293
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202167(v=OCS.15)
ms:contentKeyID: 51541449
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Backing up file stores in Lync Server 2013

 


Backing up the Lync Server File Stores includes all the files and folders used by Lync Server components.

## To back up File Stores

1.  To find the specific locations of your Lync Server File Stores, open Topology Builder and look in the **File stores** node.

2.  Use Robocopy or another file system management tool to copy each File Store to $Backup\\filestore.

