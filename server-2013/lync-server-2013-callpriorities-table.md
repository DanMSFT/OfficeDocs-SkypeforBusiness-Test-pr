---
title: 'Lync Server 2013: CallPriorities table'
TOCTitle: CallPriorities table
ms:assetid: 043b63ae-2d64-4f38-a0df-18aa08d6caf5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398093(v=OCS.15)
ms:contentKeyID: 48183275
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# CallPriorities table in Lync Server 2013

 


The CallPriorities table is a static table that stores the list of possible call priorities, such as ‘emergency’, ‘urgent’, or ‘normal’.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Data Type</th>
<th>Key/Index</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>PriorityId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><strong>Priority</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p></p></td>
<td><p>Allowed values:</p>
<ul>
<li><p>0 - Unknown</p></li>
<li><p>1 – Non-Urgent</p></li>
<li><p>2 - Normal</p></li>
<li><p>3 - Urgent</p></li>
<li><p>4 - Emergency</p></li>
</ul></td>
</tr>
</tbody>
</table>

