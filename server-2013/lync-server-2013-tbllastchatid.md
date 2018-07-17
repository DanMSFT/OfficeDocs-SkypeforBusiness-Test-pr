---
title: 'Lync Server 2013: tblLastChatId'
TOCTitle: tblLastChatId
ms:assetid: 17a4ffbe-cca9-4ec5-ae46-38a15274889a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558616(v=OCS.15)
ms:contentKeyID: 48183513
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblLastChatId in Lync Server 2013

 


tblLastChatId contains the last chat ID that was generated (and used in the tblChat table) for each user.

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
<td><p>nodeID</p></td>
<td><p>int, not null</p></td>
<td><p>Node ID (chat room-type only).</p></td>
</tr>
<tr class="even">
<td><p>lastChatID</p></td>
<td><p>bigint, not null</p></td>
<td><p>Last used chat ID.</p></td>
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
<td><p>&lt;nodeID, lastChatID&gt;</p></td>
<td><p>Primary key (just nodeID is sufficient for processing).</p></td>
</tr>
<tr class="even">
<td><p>nodeID</p></td>
<td><p>Foreign key with lookup in tblNode.nodeID table.</p></td>
</tr>
</tbody>
</table>


## See Also


[tblChat in Lync Server 2013](lync-server-2013-tblchat.md)

