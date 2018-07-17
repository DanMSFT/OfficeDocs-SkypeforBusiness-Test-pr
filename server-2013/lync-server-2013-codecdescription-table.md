---
title: 'Lync Server 2013: CodecDescription table'
TOCTitle: CodecDescription table
ms:assetid: 3598acb8-7ea6-4748-8417-149c971c32a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204797(v=OCS.15)
ms:contentKeyID: 48183802
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# CodecDescription table in Lync Server 2013

 


The CodecDescription table maps unique codec identifiers to their corresponding codec. Codecs are used to encode digital signals for transmission and broadcast, and then to decode those signals for playback. This table was introduced in Microsoft Lync Server 2013


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
<td><p><strong>CodecDescriptionKey</strong></p></td>
<td><p>smallint</p></td>
<td><p>Primary</p></td>
<td><p>Unique identifier assigned to the codec.</p></td>
</tr>
<tr class="even">
<td><p><strong>CodecDescription</strong></p></td>
<td><p>varchar(256)</p></td>
<td><p>Unique</p></td>
<td><p>Unique description of the codec corresponding to the CodecDescriptionKey.</p></td>
</tr>
</tbody>
</table>

