---
title: 'Lync Server 2013: tblComplianceState'
TOCTitle: tblComplianceState
ms:assetid: ea82e56c-3cca-4d89-b4e6-6bcaeb1f2830
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615045(v=OCS.15)
ms:contentKeyID: 48185937
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblComplianceState in Lync Server 2013

 


tblComplianceState contains pool-wide compliance state information.

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
<td><p>lastProcessedEntryID</p></td>
<td><p>bigint, not null</p></td>
<td><p>ID of the latest processed compliance event.</p></td>
</tr>
<tr class="even">
<td><p>activeServerID</p></td>
<td><p>int, not null</p></td>
<td><p>ID of the Compliance server holding the exclusive lock on the database, or -1 if none.</p></td>
</tr>
<tr class="odd">
<td><p>lockExpirationTime</p></td>
<td><p>datetime2, not null</p></td>
<td><p>Lock expiration time (if activeServerID is not -1).</p></td>
</tr>
</tbody>
</table>

