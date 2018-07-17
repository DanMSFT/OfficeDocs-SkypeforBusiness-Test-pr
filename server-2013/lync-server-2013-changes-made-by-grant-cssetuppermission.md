﻿---
title: 'Lync Server 2013: Changes made by Grant-CsSetupPermission'
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Changes made by Grant-CsSetupPermission in Lync Server 2013

 


To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.

The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:

### Permissions granted to Objects in the OU

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Permissions apply to:</th>
<th>Permissions granted are:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RTCUniversalServerAdmins</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Read servicePrincipalName</p></li>
<li><p>Write servicePrincipalName</p></li>
<li><p>Delete tree</p></li>
<li><p>Replicating directory changes</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Descendant serviceConnectionPoint objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Read permissions</p></li>
<li><p>Write permissions</p></li>
<li><p>Create child</p></li>
<li><p>Delete child</p></li>
<li><p>List contents</p></li>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Descendant msRTCSIP-Server objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Descendant msRTCSIP-WebComponents objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Descendant msRTCSIP-MCU objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Descendant msRTCSIP-MediationServer objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Descendant msRTCSIP-ApplicationServer objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Descendant msRTCSIP-ConnectionPoint objects</p></td>
<td><p>Special access:</p>
<ul>
<li><p>Write property</p></li>
<li><p>Read property</p></li>
<li><p>Delete tree</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Descendant Computer objects</p></td>
<td><p>Special access for serviceConnectionPoint:</p>
<ul>
<li><p>Create child objects</p></li>
<li><p>Delete child objects</p></li>
<li><p>Delete tree</p></li>
</ul>
<p>Special access for public information:</p>
<ul>
<li><p>Read property</p></li>
</ul>
<p>Special access for DNS host name:</p>
<ul>
<li><p>Read property</p></li>
</ul></td>
</tr>
</tbody>
</table>

