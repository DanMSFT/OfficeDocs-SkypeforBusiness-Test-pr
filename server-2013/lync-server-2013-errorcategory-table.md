---
title: 'Lync Server 2013: ErrorCategory table'
TOCTitle: ErrorCategory table
ms:assetid: 0fde3b73-9a2f-44dd-b8dc-6df512303ff1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204675(v=OCS.15)
ms:contentKeyID: 48183425
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# ErrorCategory table in Lync Server 2013

 


The ErrorCategory table contains the friendly name for each Microsoft Lync Server 2013 diagnostic classification. By default, Lync Server 2013 uses the following classifications:

  - 0 -- Success

  - 1 -- Expected failure

  - 2 – Unexpected failure

This table was introduced in Microsoft Lync Server 2013.


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
<td><p><strong>CategoryId</strong></p></td>
<td><p>tinyint</p></td>
<td><p>Primary</p></td>
<td><p>Unique identifier for the classification.</p></td>
</tr>
<tr class="even">
<td><p><strong>Name</strong></p></td>
<td><p>nvarchar(256)</p></td>
<td><p></p></td>
<td><p>Value and friendly name assigned to the classification. Allowed values are:</p>
<ul>
<li><p>0 -- Success</p></li>
<li><p>1 -- Expected failure</p></li>
<li><p>2 – Unexpected failure</p></li>
</ul></td>
</tr>
</tbody>
</table>

