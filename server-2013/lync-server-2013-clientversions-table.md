---
title: 'Lync Server 2013: ClientVersions table'
TOCTitle: ClientVersions table
ms:assetid: 542316cf-a6db-4d52-ab28-8bf6d27a3b48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398356(v=OCS.15)
ms:contentKeyID: 48184176
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# ClientVersions table in Lync Server 2013

 


The ClientVersions table is a supporting table that stores a list of the various client types and versions that have participated in sessions recorded in the database. Each record in the table represents one client version.


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
<td><p><strong>VersionId</strong></p></td>
<td><p><strong>int</strong></p></td>
<td><p>Primary</p></td>
<td><p>Unique number identifying this client type and version.</p></td>
</tr>
<tr class="even">
<td><p><strong>Version</strong></p></td>
<td><p><strong>nvarchar(256)</strong></p></td>
<td><p></p></td>
<td><p>Version name.</p></td>
</tr>
<tr class="odd">
<td><p><strong>ClientType</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>Specifies the type of client used in the session. See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</p>
<p>This field was introduced in Microsoft Lync Server 2013.</p></td>
</tr>
</tbody>
</table>

