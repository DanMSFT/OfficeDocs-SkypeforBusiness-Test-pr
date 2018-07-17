---
title: 'Lync Server 2013: Gateways table'
TOCTitle: Gateways table
ms:assetid: a909daad-d137-45e0-b149-1de9f8e1e029
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412795(v=OCS.15)
ms:contentKeyID: 48185034
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Gateways table in Lync Server 2013

 


The Gateways table is a supporting table. Each record stores information about one gateway that is involved in public switched telephone network (PSTN) calls that have records in the database.


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
<td><p><strong>GatewayId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this gateway.</p></td>
</tr>
<tr class="even">
<td><p><strong>Gateway</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p> </p></td>
<td><p>Gateway name.</p></td>
</tr>
</tbody>
</table>

