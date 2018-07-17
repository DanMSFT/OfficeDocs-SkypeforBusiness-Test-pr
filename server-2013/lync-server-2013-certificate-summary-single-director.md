---
title: 'Lync Server 2013: Certificate summary - Single Director'
TOCTitle: Certificate summary - Single Director
ms:assetid: 1b769a76-cbf3-46e9-a955-f6cde5faff93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204720(v=OCS.15)
ms:contentKeyID: 48183546
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Certificate summary - Single Director in Lync Server 2013

 


Certificate requirements for a single Director consist of a default certificate that has a subject name and subject alternative names for services that the Director can receive. Additionally, there is an OAuth Token certificate for server to server authentication purposes.

### Certificates for Director

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
<td><p>dir01.contoso.net</p></td>
<td><p>dir01.contoso.net</p>
<p>dialin.contoso.com</p>
<p>meet.contoso.com</p>
<p>lyncdiscoverinternal.contoso.com</p>
<p>lyncdiscover.contoso.com</p>
<p>(Optionally) *.contoso.com</p></td>
<td><p>Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</p>
<p>The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server. Internal clients will not use the Director.</p>
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

<p>The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA. The certificate is required.</p>
<p></p></td>
</tr>
</tbody>
</table>

