---
title: 'Lync Server 2013: MediationServers table'
TOCTitle: MediationServers table
ms:assetid: 9f757377-ab79-4795-aaa9-1163cb9c8a59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412743(v=OCS.15)
ms:contentKeyID: 48184929
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# MediationServers table in Lync Server 2013

 


The MediationServers table is a supporting table. Each record stores information about one Mediation Server that is involved in calls that have records in the database.


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
<td><p><strong>MediationServerId</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this Mediation Server.</p></td>
</tr>
<tr class="even">
<td><p><strong>MediationServer</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p> </p></td>
<td><p>Mediation Server name.</p></td>
</tr>
</tbody>
</table>

