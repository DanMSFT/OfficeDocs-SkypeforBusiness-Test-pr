---
title: 'Lync Server 2013: UserAgent view'
TOCTitle: UserAgent view
ms:assetid: b986f76f-f16e-4e5e-96cb-6e8f7f9b42ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721862(v=OCS.15)
ms:contentKeyID: 49733795
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# UserAgent view in Lync Server 2013

 


The UserAgent View stores information about the user agents that have been involved in sessions that have records in the database. This view was introduced in Microsoft Lync Server 2013.


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Data Type</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>UserAgentKey</p></td>
<td><p>int</p></td>
<td><p>Unique number identifying this user agent.</p></td>
</tr>
<tr class="even">
<td><p>UserAgent</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>User agent string.</p></td>
</tr>
<tr class="odd">
<td><p>UAType</p></td>
<td><p>smallint</p></td>
<td><p>Type of user agent. See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for more details.</p></td>
</tr>
<tr class="even">
<td><p>UACategory</p></td>
<td><p>nvarchar(64)</p></td>
<td><p>Category that the user agent belongs to. For example, the user agent Conferencing_Attendant_1.0 belongs to the UACategory CAA.</p></td>
</tr>
</tbody>
</table>

