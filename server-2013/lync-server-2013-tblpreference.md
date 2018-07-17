---
title: 'Lync Server 2013: tblPreference'
TOCTitle: tblPreference
ms:assetid: f94eb128-f782-42ff-a568-ed3529573bc8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615052(v=OCS.15)
ms:contentKeyID: 48185913
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblPreference in Lync Server 2013

 


tblPreference contains the users’ client preferences. This is generally used by clients previous to Lync 2013.

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
<td><p>prefLabel</p></td>
<td><p>nvarchar (255), not null</p></td>
<td><p>Label with a format such as: &lt;user sip uri&gt;|username.&lt;preference set&gt;.</p></td>
</tr>
<tr class="even">
<td><p>prefSeqID</p></td>
<td><p>int, not null</p></td>
<td><p>A sequential number (per label) for versioning purposes.</p></td>
</tr>
<tr class="odd">
<td><p>prefContent</p></td>
<td><p>nvarchar (max)</p></td>
<td><p>Encoded content.</p></td>
</tr>
<tr class="even">
<td><p>lastModifiedBy</p></td>
<td><p>int, not null</p></td>
<td><p>ID of the principal that updated the preference.</p></td>
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
<td><p>&lt;prefLabel, prefSeqID&gt;</p></td>
<td><p>Primary key.</p></td>
</tr>
</tbody>
</table>

