---
title: 'Lync Server 2013: tblPrincipalType'
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# tblPrincipalType in Lync Server 2013

 


tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.

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
<td><p>ptypeID</p></td>
<td><p>smallint, not null</p></td>
<td><p>Principal type ID.</p></td>
</tr>
<tr class="even">
<td><p>ptypeDesc</p></td>
<td><p>nvarchar (256), not null</p></td>
<td><p>Description of the type.</p></td>
</tr>
<tr class="odd">
<td><p>ptypeIsSystemUser</p></td>
<td><p>bit, not null</p></td>
<td><p>True if the type corresponds to the principals that are used for internal purposes.</p></td>
</tr>
<tr class="even">
<td><p>ptypeIsUser</p></td>
<td><p>bit, not null</p></td>
<td><p>True if the type is a user type.</p></td>
</tr>
</tbody>
</table>


### Key

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Column</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ptypeID</p></td>
<td><p>Primary key.</p></td>
</tr>
</tbody>
</table>


### Principal Values

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>ID</th>
<th>Role</th>
<th>Description</th>
<th>User</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>Any</p></td>
<td><p>Generic principal with no known type. Not used in tblPrincipal table.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>AnyUser</p></td>
<td><p>Generic principal of user type. Not used in tblPrincipal table.</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>AnyGroup</p></td>
<td><p>Generic principal with group semantic. Not used in tblPrincipal table.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>SystemUser</p></td>
<td><p>Principal used internally by Persistent Chat Server.</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>User</p></td>
<td><p>Regular user.</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p>DC</p></td>
<td><p>Active Directory Domain Services domain controller.</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>9</p></td>
<td><p>Group</p></td>
<td><p>Active Directory security group.</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>10</p></td>
<td><p>Folder</p></td>
<td><p>Active Directory container or organizational unit.</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## See Also


[tblPrincipal in Lync Server 2013](lync-server-2013-tblprincipal.md)

