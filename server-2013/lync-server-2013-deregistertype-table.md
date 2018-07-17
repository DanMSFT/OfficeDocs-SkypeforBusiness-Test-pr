---
title: 'Lync Server 2013: DeRegisterType table'
TOCTitle: DeRegisterType table
ms:assetid: 09148118-6209-4fd7-a494-99118689a245
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398142(v=OCS.15)
ms:contentKeyID: 48183346
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# DeRegisterType table in Lync Server 2013

 


The DeRegisterType table is a static table that stores the list of possible user de-registers types, such as ‘client initiated’, ‘registration expired’, or ‘client stopped responding.’


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
<td><p><strong>DeRegisterTypeId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><strong>DeRegisterReason</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p></p></td>
<td><p>Allowed values:</p>
<ul>
<li><p>0 -- Unknown</p></li>
<li><p>1 -- Client Initiated Deregistration</p></li>
<li><p>2 -- Registration Expired</p></li>
<li><p>3 – Client crashed</p></li>
<li><p>4 -- User Attributes Changed</p></li>
<li><p>5 – Preferred Registrar Changed</p></li>
<li><p>6 -- Legacy Client In Survival Mode</p></li>
</ul></td>
</tr>
</tbody>
</table>

