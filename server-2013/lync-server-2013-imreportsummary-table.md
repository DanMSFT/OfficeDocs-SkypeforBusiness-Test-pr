﻿---
title: 'Lync Server 2013: IMReportSummary table'
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# IMReportSummary table in Lync Server 2013

 


The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization. This table was introduced in Microsoft Lync Server 2013.


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
<td><p><strong>StartTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Primary</p></td>
<td><p>Date and time that the instant messaging session began.</p></td>
</tr>
<tr class="even">
<td><p><strong>TimePeriod</strong></p></td>
<td><p>char(1)</p></td>
<td><p>Primary</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><strong>PoolFQDN</strong></p></td>
<td><p>nvarchar(257)</p></td>
<td><p>Primary</p></td>
<td><p>Fully qualified domain name of the pool hosting the session.</p></td>
</tr>
<tr class="even">
<td><p><strong>AuthType</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Priority (for example, urgent or non-urgent) of the call. Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>SessionCount</strong></p></td>
<td><p>bigint</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><strong>MsgCount</strong></p></td>
<td><p>bigint</p></td>
<td><p></p></td>
<td><p>Total number of instant messages exchanged during the session.</p></td>
</tr>
</tbody>
</table>

