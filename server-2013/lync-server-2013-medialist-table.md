---
title: 'Lync Server 2013: MediaList table'
TOCTitle: MediaList table
ms:assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398279(v=OCS.15)
ms:contentKeyID: 48183579
ms.date: 07/12/2016
mtps_version: v=OCS.15
---

# MediaList table in Lync Server 2013

 


The MediaList table is a static table that stores the list of various media types.


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
<td><p><strong>MediaId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>Values: 1-7</p></td>
</tr>
<tr class="even">
<td><p><strong>Media</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p></p></td>
<td><p>Static mapping of MediaID and Media values:</p>
<ul>
<li><p>1 – IM</p></li>
<li><p>2 – File Transfer</p></li>
<li><p>3 – Remote Assistance</p></li>
<li><p>4 – Application Sharing</p></li>
<li><p>5 – Audio</p></li>
<li><p>6 – Video</p></li>
<li><p>7 – App Invite</p></li>
</ul></td>
</tr>
</tbody>
</table>


If you are trying to determine the modality type for the values in LcsCDR.SessionDetailsView.MediaTypes, then you need to use the following Join snippet:

    LEFT JOIN on Media.MediaId = MediaList.MediaId

