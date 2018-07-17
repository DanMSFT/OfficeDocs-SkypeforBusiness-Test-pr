﻿---
title: 'Lync Server 2013: VoipDetails table'
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# VoipDetails table in Lync Server 2013

 


Each record represents one two-party call in which at least one user is a VoIP user.


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
<td><p><strong>SessionIdTime</strong></p></td>
<td><p>datetime</p></td>
<td><p>Primary</p></td>
<td><p>Time of session request. Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session. See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="even">
<td><p><strong>SessionIdSeq</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>ID number to identify the session. Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session. See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="odd">
<td><p><strong>FromNumberId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p><strong>PhoneId</strong> of the caller. See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information. If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</p></td>
</tr>
<tr class="even">
<td><p><strong>ConnectedNumberId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p><strong>PhoneId</strong> of the call receiver. See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information. If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</p></td>
</tr>
<tr class="odd">
<td><p><strong>FromMediationServerId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p>The Mediation Server the call is coming from. See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="even">
<td><p><strong>ToMediationServerId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p>The Mediation Server called is going to. See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="odd">
<td><p><strong>FromGatewayId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p>Gateway the call is coming from. See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="even">
<td><p><strong>ToGatewayId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p>Gateway the call is going to. See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DisconnectedbyURIId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p>URI of the user who disconnected the call, if the user has a URI. See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</p></td>
</tr>
<tr class="even">
<td><p><strong>DisconnectedbyPhoneId</strong></p></td>
<td><p>int</p></td>
<td><p>Foreign</p></td>
<td><p>ID of the phone that disconnected the call was disconnected from a phone. See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</p></td>
</tr>
</tbody>
</table>

