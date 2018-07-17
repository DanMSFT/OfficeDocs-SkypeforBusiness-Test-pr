---
title: 'Lync Server 2013: tblLastInviteId'
TOCTitle: tblLastInviteId
ms:assetid: 222b3508-5963-4ddc-b4f3-e8412767e61b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558625(v=OCS.15)
ms:contentKeyID: 48183608
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblLastInviteId in Lync Server 2013

 


tblLastInviteId contains the last invite ID that was generated (and used in the tblPrincipalInvites table) for each user.

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
<td><p>prinID</p></td>
<td><p>int, not null</p></td>
<td><p>Principal ID.</p></td>
</tr>
<tr class="even">
<td><p>lastInviteID</p></td>
<td><p>int, not null</p></td>
<td><p>Last used invite ID.</p></td>
</tr>
</tbody>
</table>


### Keys

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>prinID</p></td>
<td><p>Primary key.</p></td>
</tr>
<tr class="even">
<td><p>prinID</p></td>
<td><p>Foreign key with lookup in tblPrincipal.prinID table.</p></td>
</tr>
</tbody>
</table>


## See Also


[tblPrincipalInvites in Lync Server 2013](lync-server-2013-tblprincipalinvites.md)

