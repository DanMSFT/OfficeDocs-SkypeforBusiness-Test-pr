---
title: 'Lync Server 2013: Endpoint table'
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Endpoint table in Lync Server 2013

 


The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database. Each record in the table represents one endpoint.


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
<td><p><strong>EndpointKey</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this endpoint.</p></td>
</tr>
<tr class="even">
<td><p><strong>Name</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Unique</p></td>
<td><p>Endpoint name.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OS</strong></p></td>
<td><p>nvarchar(128)</p></td>
<td><p> </p></td>
<td><p>Operating system (OS) of the endpoint.</p></td>
</tr>
<tr class="even">
<td><p><strong>CPUName</strong></p></td>
<td><p>nvarchar(128)</p></td>
<td><p></p></td>
<td><p>CPU name of the endpoint.</p></td>
</tr>
<tr class="odd">
<td><p><strong>CPUNumberOfCores</strong></p></td>
<td><p>smallint</p></td>
<td><p></p></td>
<td><p>Number of CPU cores of the endpoint.</p></td>
</tr>
<tr class="even">
<td><p><strong>CPUProcessorSpeed</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>CPU processor speed of the endpoint.</p></td>
</tr>
<tr class="odd">
<td><p><strong>VirtualizationFlag</strong></p></td>
<td><p>tinyint</p></td>
<td><p></p></td>
<td><p>Bit flag that indicates if the system is running in a virtualized environment:</p>
<ul>
<li><p>0x0000 – None</p></li>
<li><p>0x0001 – HyperV</p></li>
<li><p>0x0002 – VMWare</p></li>
<li><p>0x0004 – Virtual PC</p></li>
<li><p>0x0008 – Xen PC</p></li>
</ul></td>
</tr>
</tbody>
</table>

