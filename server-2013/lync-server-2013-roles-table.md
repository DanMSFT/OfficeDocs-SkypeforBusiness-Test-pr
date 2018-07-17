---
title: 'Lync Server 2013: Roles table'
TOCTitle: Roles table
ms:assetid: e8eb8a10-26b5-488b-bc8c-f9ef93f98bdb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399043(v=OCS.15)
ms:contentKeyID: 48185893
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Roles table in Lync Server 2013

 


The Roles table is a static table that stores the list of possible conference roles, such as attendee and presenter.


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
<td><p><strong>RoleId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><strong>Role</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p></p></td>
<td><p>Allowed values:</p>
<ul>
<li><p>0 - Unknown</p></li>
<li><p>1 - Presenter</p></li>
<li><p>2 - Attendee</p></li>
</ul></td>
</tr>
</tbody>
</table>

