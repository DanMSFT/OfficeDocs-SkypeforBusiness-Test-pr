---
title: 'Lync Server 2013: PurgeSettings table'
TOCTitle: PurgeSettings table
ms:assetid: 9ff2c8fc-4ae8-4f22-96a8-1f4d5eecbf2d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205121(v=OCS.15)
ms:contentKeyID: 48184932
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# PurgeSettings table in Lync Server 2013

 


The PurgeSettings table contains information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database. Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:

    Get-CsCdrConfiguration

Administrators should treat the PurgeSettings table as read-only: changes to the call detail purge settings should only be made using the [New-CsCdrConfiguration](https://technet.microsoft.com/en-us/library/gg399018\(v=ocs.15\)) or [Set-CsCdrConfiguration](https://technet.microsoft.com/en-us/library/gg398774\(v=ocs.15\)) cmdlets.

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
<td><p><strong>Id</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Unique identifier for the collection of CDR purge settings.</p></td>
</tr>
<tr class="even">
<td><p><strong>EnablePurge</strong></p></td>
<td><p>bit</p></td>
<td><p></p></td>
<td><p>When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the CDR database. Purging will take place each day at the tome specified by the PurgeHour setting. If set to False (0) then records will not be automatically purged from the database. The default value is True.</p></td>
</tr>
<tr class="odd">
<td><p><strong>KeepCallDetailForDays</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>Specifies the age of CDR records (in days) that will be purged from the database: if purging is enabled, CDR records older than this value will be removed from the database. The default value is 60 days.</p></td>
</tr>
<tr class="even">
<td><p><strong>KeepErrorReportForDays</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>Specifies the age of error report records (in days) that will be purged from the database: if purging is enabled, error report records older than this value will be removed from the database. The default value is 60 days.</p></td>
</tr>
<tr class="odd">
<td><p><strong>PurgeHour</strong></p></td>
<td><p>int</p></td>
<td><p></p></td>
<td><p>Specifies the local time of day when database purging will take place. The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM. Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed. The default value is 2 (2:00 AM).</p></td>
</tr>
</tbody>
</table>

