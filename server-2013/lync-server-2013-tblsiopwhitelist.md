---
title: 'Lync Server 2013: tblSiopWhiteList'
TOCTitle: tblSiopWhiteList
ms:assetid: 05fc1df4-32eb-4d46-9d1c-e0b607091142
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558607(v=OCS.15)
ms:contentKeyID: 48183310
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblSiopWhiteList in Lync Server 2013

 


tblSiopWhiteList is the list of registered add-ins that can be associated with nodes.

### Columns

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>siopID</p></td>
<td><p>GUID, not null</p></td>
<td><p>GUID of the add-in.</p></td>
</tr>
<tr class="even">
<td><p>siopName</p></td>
<td><p>nvarchar (50), not null</p></td>
<td><p>Display-name of the add-in.</p></td>
</tr>
<tr class="odd">
<td><p>siopUrl</p></td>
<td><p>nvarchar (255), not null</p></td>
<td><p>URL of the add-in.</p></td>
</tr>
</tbody>
</table>


### Key

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>siopID</p></td>
<td><p>Primary key.</p></td>
</tr>
</tbody>
</table>

