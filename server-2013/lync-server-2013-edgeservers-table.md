﻿---
title: 'Lync Server 2013: EdgeServers table'
TOCTitle: EdgeServers table
ms:assetid: aeda8c01-c88c-4f56-b3d0-bac475fae449
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412833(v=OCS.15)
ms:contentKeyID: 48185081
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# EdgeServers table in Lync Server 2013

 


The EdgeServers table is a supporting table. Each record stores information about one Edge Server that is involved in calls that have records in the database.


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
<td><p><strong>EdgeServerId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this Edge Server.</p></td>
</tr>
<tr class="even">
<td><p><strong>EdgeServer</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p> </p></td>
<td><p>Edge Server name.</p></td>
</tr>
</tbody>
</table>

