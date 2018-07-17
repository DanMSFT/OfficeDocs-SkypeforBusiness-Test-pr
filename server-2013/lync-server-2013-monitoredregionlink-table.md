---
title: 'Lync Server 2013: MonitoredRegionLink table'
TOCTitle: MonitoredRegionLink table
ms:assetid: cebda194-7be3-42d6-b6f0-c86f8b0f200a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398874(v=OCS.15)
ms:contentKeyID: 48185487
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# MonitoredRegionLink table in Lync Server 2013

 


The MonitoredRegionLink table is a supporting table. Each record represents one link between two countries/regions.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Column</strong></th>
<th><strong>Data Type</strong></th>
<th><strong>Key/Index</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Region1Key</strong></p></td>
<td><p>int</p></td>
<td><p>Primary, Foreign</p></td>
<td><p>Referenced from the <a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Region2Key</strong></p></td>
<td><p>int</p></td>
<td><p>Primary, Foreign</p></td>
<td><p>Referenced from the <a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a>.</p></td>
</tr>
</tbody>
</table>

