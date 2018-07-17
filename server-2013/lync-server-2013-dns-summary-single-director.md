﻿---
title: 'Lync Server 2013: DNS summary - Single Director'
TOCTitle: DNS summary - Single Director
ms:assetid: 790ecb56-92cd-41f4-baf6-c290a707aa4d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205021(v=OCS.15)
ms:contentKeyID: 48184568
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# DNS summary - Single Director in Lync Server 2013

 


The following table contains a summary of the DNS records that are required to support the single Director. The role of the Director requires similar DNS records as the Front End Server. The number of records needed is reflected in the subject alternative names required on the Director certificate. Different from the Front End Server, the Director does not host user accounts or host the Mobility Services.

### DNS Records Required for the Director

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Location/TYPE/Port</th>
<th>FQDN/DNS Record</th>
<th>IP Address/FQDN</th>
<th>Maps to/Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Internal DNS/A</p></td>
<td><p>dir01.contoso.net</p></td>
<td><p>Director</p></td>
<td><p>Director host record used for replication and server to server</p></td>
</tr>
<tr class="even">
<td><p>Internal DNS/A</p></td>
<td><p>sip.contoso.com</p></td>
<td><p>Director</p></td>
<td><p>Inbound session initiation protocol (SIP) from the internal Edge interface of the Edge Server</p></td>
</tr>
<tr class="odd">
<td><p>Internal DNS/A</p></td>
<td><p>dialin.contoso.com</p></td>
<td><p>Director</p></td>
<td><p>Published dialin web services from reverse proxy</p></td>
</tr>
<tr class="even">
<td><p>Internal DNS/A</p></td>
<td><p>meet.contoso.com</p></td>
<td><p>Director</p></td>
<td><p>Published meet web services from reverse proxy</p></td>
</tr>
<tr class="odd">
<td><p>Internal DNS/A</p></td>
<td><p>webdirexternal.contoso.com</p></td>
<td><p>Director</p></td>
<td><p>Published and defined by the reverse proxy Web Ticket external web services for the Director</p></td>
</tr>
</tbody>
</table>

