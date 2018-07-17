﻿---
title: 'Lync Server 2013: List of Persistent Chat Server compliance tables'
TOCTitle: List of Persistent Chat Server compliance tables
ms:assetid: 8563446e-90cc-47cc-8a8e-4883decfe195
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215878(v=OCS.15)
ms:contentKeyID: 48706007
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# List of Persistent Chat Server compliance tables in Lync Server 2013

 


The Persistent Chat compliance database schema consists of the following tables.

## List of Persistent Chat Server Compliance Tables


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Table</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="lync-server-2013-tblcompliancedata.md">tblComplianceData in Lync Server 2013</a></p></td>
<td><p>Contains the compliance events that have not yet been processed by the configured adapter.</p>
<p>This table includes Persistent Chat-related events, such as chat messages and file downloads. (Participant events are tracked by the tblComplianceParticipant table.)</p>
<p>(The servers that processed the events in this table are listed in the tblComplianceFanout table.)</p></td>
</tr>
<tr class="even">
<td><p><a href="lync-server-2013-tblcompliancefanout.md">tblComplianceFanout in Lync Server 2013</a></p></td>
<td><p>Contains the servers that processed a compliance event. This table is tightly coupled with the tblComplianceData table.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lync-server-2013-tblcomplianceparticipant.md">tblComplianceParticipant in Lync Server 2013</a></p></td>
<td><p>Contains current participants per chat service and per server. It is maintained based on join and part compliance events received from the Persistent Chat service.</p></td>
</tr>
<tr class="even">
<td><p><a href="lync-server-2013-tblcompliancestate.md">tblComplianceState in Lync Server 2013</a></p></td>
<td><p>Contains pool-wide compliance state information.</p></td>
</tr>
</tbody>
</table>

