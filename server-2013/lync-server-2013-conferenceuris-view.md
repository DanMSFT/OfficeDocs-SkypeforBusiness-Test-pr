---
title: 'Lync Server 2013: ConferenceUris view'
TOCTitle: ConferenceUris view
ms:assetid: 9a3cdcea-426e-4b6b-9876-ba746a8de706
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688148(v=OCS.15)
ms:contentKeyID: 49733750
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# ConferenceUris view in Lync Server 2013

 


The ConfernceUris view stores information about the URIs that have participated in conference sessions. This view was introduced in Microsoft Lync Server 2013.


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
<td><p>ConferenceUriId</p></td>
<td><p>int</p></td>
<td><p>Unique number identifying the conference URI.</p></td>
</tr>
<tr class="even">
<td><p>ConferenceUri</p></td>
<td><p>nvarchar(450)</p></td>
<td><p>URI of the conference.</p></td>
</tr>
<tr class="odd">
<td><p>ConferenceUriType</p></td>
<td><p>nvarchar(256)</p></td>
<td><p>Type of conference URI. See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</p></td>
</tr>
</tbody>
</table>

