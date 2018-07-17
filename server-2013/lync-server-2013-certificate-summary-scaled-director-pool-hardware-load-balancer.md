---
title: 'Lync Server 2013: Certificate summary - Scaled Director pool, hardware load balancer'
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013

 


Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive. A certificate is requested for each Director in the pool. Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.

### Certificates for a Scaled Director Using a Hardware Load Balancer

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Component</th>
<th>Subject name (SN)</th>
<th>Subject alternative names (SAN)</th>
<th>Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Default</p></td>
<td><p>dirpool01.contoso.net</p></td>
<td><p>dirpool01.contoso.net</p>
<p>dir01.contoso.net</p>
<p>dialin.contoso.com</p>
<p>meet.contoso.com</p>
<p>lyncdiscoverinternal.contoso.com</p>
<p>lyncdiscover.contoso.com</p>
<p>(Optionally) *.contoso.com</p></td>
<td><p>Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</p>
<p>The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</p>
<p>Or, a wildcard entry for the simple URLs</p></td>
</tr>
<tr class="even">
<td><p>OAuthTokenIssuer</p></td>
<td><p>dir01.contoso.net</p></td>
<td><p>No Entry</p></td>
<td><table>
<thead>
<tr class="header">
<th><img src="images/Gg412910.important(OCS.15).gif" title="important" alt="important" />Important:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</td>
</tr>
</tbody>
</table>

<p>The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA. The certificate is required.</p></td>
</tr>
</tbody>
</table>

