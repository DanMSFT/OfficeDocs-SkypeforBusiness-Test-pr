---
title: 'Lync Server 2013: Servers table'
TOCTitle: Servers table
ms:assetid: 1535e676-a647-4606-bc56-e8bfde5ca823
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398223(v=OCS.15)
ms:contentKeyID: 48183487
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Servers table in Lync Server 2013

 


The Servers table is a supporting table that stores information about the various servers. Each record in the table represents one server.


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
<td><p><strong>ServerId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this server.</p></td>
</tr>
<tr class="even">
<td><p><strong>ServerFQDN</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p> </p></td>
<td><p>Server FQDN.</p></td>
</tr>
</tbody>
</table>

