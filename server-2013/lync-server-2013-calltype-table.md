---
title: 'Lync Server 2013: CallType table'
TOCTitle: CallType table
ms:assetid: a1d7187c-f851-4967-88ea-73922911ee7a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412752(v=OCS.15)
ms:contentKeyID: 48185019
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# CallType table in Lync Server 2013

 


The CallType table is a static table that stores the list of possible call types.


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
<td><p><strong>CallTypeId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><strong>CallType</strong></p></td>
<td><p>nvarchar</p></td>
<td><p></p></td>
<td><p>Allowed values:</p>
<ul>
<li><p>0 -- Unknown</p></li>
<li><p>1 – Instant Messaging</p></li>
<li><p>2 -- Application Sharing</p></li>
<li><p>3 -- Audio</p></li>
<li><p>4 – Audio and Video</p></li>
<li><p>5 – File Transfer</p></li>
</ul></td>
</tr>
</tbody>
</table>

