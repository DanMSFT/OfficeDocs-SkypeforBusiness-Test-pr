﻿---
title: 'Lync Server 2013: Pools table'
TOCTitle: Pools table
ms:assetid: e0632b8d-e23a-4365-8a7a-6ca0957a46a9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398991(v=OCS.15)
ms:contentKeyID: 48185680
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Pools table in Lync Server 2013

 


The Pools table is a supporting table that stores information about the various pool. Each record in the table represents one pool.


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
<td><p><strong>PoolId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this pool.</p></td>
</tr>
<tr class="even">
<td><p><strong>PoolFQDN</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p> </p></td>
<td><p>Pool FQDN.</p></td>
</tr>
</tbody>
</table>

