---
title: 'Lync Server 2013: Capacity planning for Call Park'
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Capacity planning for Call Park in Lync Server 2013

 


The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.


> [!IMPORTANT]
> Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.



### Call Park User Model

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metric</th>
<th>Per Front End pool (with 8 Front End Servers)</th>
<th>Per Standard Edition server</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Park rate</p></td>
<td><p>8 per minute</p></td>
<td><p>1 per minute</p></td>
</tr>
<tr class="even">
<td><p>Retrieve parked call rate</p></td>
<td><p>8 per minute</p></td>
<td><p>1 per minute</p></td>
</tr>
<tr class="odd">
<td><p>Average park duration</p></td>
<td><p>60 seconds</p></td>
<td><p>60 seconds</p></td>
</tr>
</tbody>
</table>

