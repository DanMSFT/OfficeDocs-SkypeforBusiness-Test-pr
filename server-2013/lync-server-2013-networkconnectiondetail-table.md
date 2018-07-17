---
title: 'Lync Server 2013: NetworkConnectionDetail table'
TOCTitle: NetworkConnectionDetail table
ms:assetid: b48cc9a6-5232-48b5-bd20-53b68229336b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205185(v=OCS.15)
ms:contentKeyID: 48185170
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# NetworkConnectionDetail table in Lync Server 2013

 


The NetworkConnectionDetail table maps network connection types to the network connection identifiers used elsewhere in the Quality of Experience database. This table was introduced in Microsoft Lync Server 2013.


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
<td><p><strong>NetworkConnectionDetailKey</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>Unique identifier for the network connection type.</p></td>
</tr>
<tr class="even">
<td><p><strong>NetworkConnectionDetail</strong></p></td>
<td><p>varchar(256)</p></td>
<td><p>Unique</p></td>
<td><p>Network connection type that corresponds to the NetworkConnectionDetailKey. Allowed values are:</p>
<ol>
<li><p>0 -- Wired</p></li>
<li><p>1 -- WiFi</p></li>
<li><p>2 -- Ethernet</p></li>
</ol></td>
</tr>
</tbody>
</table>

