---
title: 'Lync Server 2013: tblAdminLock'
TOCTitle: tblAdminLock
ms:assetid: 785a43c0-6892-474c-821c-fa9cdbeb99d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558665(v=OCS.15)
ms:contentKeyID: 48184560
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblAdminLock in Lync Server 2013

 


tblAdminLock contains the administrator lock that is needed to run some administrator commands.

### Columns

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>lockExpiresTime</p></td>
<td><p>datetime, not null</p></td>
<td><p>Lock expiration date and time. The owner can extend this value periodically.</p></td>
</tr>
<tr class="even">
<td><p>lockServerID</p></td>
<td><p>int, not null</p></td>
<td><p>ID of the server that owns the lock.</p></td>
</tr>
<tr class="odd">
<td><p>lockActorID</p></td>
<td><p>int, not null</p></td>
<td><p>ID of the principal that owns the lock.</p></td>
</tr>
</tbody>
</table>

