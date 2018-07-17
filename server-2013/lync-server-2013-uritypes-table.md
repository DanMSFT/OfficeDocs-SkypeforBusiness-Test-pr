---
title: 'Lync Server 2013: UriTypes table'
TOCTitle: UriTypes table
ms:assetid: 77c4dfae-1b29-4e81-ba05-609e61643998
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398587(v=OCS.15)
ms:contentKeyID: 48184553
ms.date: 06/16/2015
mtps_version: v=OCS.15
---

# UriTypes table in Lync Server 2013

 


The UriTypes Table contains the different URI (Uniform resource identifier) types monitored in Microsoft Lync Server 2013.


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
<td><p><strong>UriTypeId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>Unique identifier assigned to a URI type.</p></td>
</tr>
<tr class="even">
<td><p><strong>UriType</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p></p></td>
<td><p>Descriptions of the different URI types. Allowed values are:</p>
<ul>
<li><p>1 – Phone Uri</p></li>
<li><p>0 – User Uri</p></li>
</ul></td>
</tr>
</tbody>
</table>

