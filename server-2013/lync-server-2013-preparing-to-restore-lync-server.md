﻿---
title: 'Lync Server 2013: Preparing to restore Lync Server'
TOCTitle: Preparing to restore Lync Server
ms:assetid: 857e4e02-908e-433a-96c6-be1795a9cb61
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202179(v=OCS.15)
ms:contentKeyID: 51541490
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Preparing to restore Lync Server 2013

 


Before you begin restoring servers and databases after a failure, you need to determine the following:

  - What needs to be restored.

  - The hardware, software, data, and tools you need for restoration.

## Determining What to Restore

This topic describes how to restore Lync Server outages that occur at the server, pool, or Central Management store level. If the Central Management store fails, your Lync Server deployment continues to function, but you cannot make any configuration changes. If a Back End Server or Standard Edition server fails, the user pool stops functioning. If any other server fails, the magnitude of the failure depends on the server role the server is running and whether the server hosts one or more databases.

### What to Restore

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>If this failed</th>
<th>See this section:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Standard Edition server</p></td>
<td><p><a href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</a></p></td>
</tr>
<tr class="even">
<td><p>Central Management store</p></td>
<td><p><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Restoring the server hosting the Central Management store in Lync Server 2013</a></p></td>
</tr>
<tr class="odd">
<td><p>Enterprise Edition Back End</p></td>
<td><p><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</a></p></td>
</tr>
<tr class="even">
<td><p>Enterprise Edition Mirrored Back End Primary Server</p></td>
<td><p><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary</a></p></td>
</tr>
<tr class="odd">
<td><p>Enterprise Edition Mirrored Back End Secondary Server</p></td>
<td><p><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</a></p></td>
</tr>
<tr class="even">
<td><p>Any Enterprise Edition server running a server role, such as a Front End Server, Edge Server, Director, Mediation Server,.or Persistent Chat Server.</p></td>
<td><p><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</a></p></td>
</tr>
<tr class="odd">
<td><p>An entire Lync Server pool</p></td>
<td><p><a href="lync-server-2013-restoring-a-lync-server-pool.md">Restoring a Lync Server pool in Lync Server 2013</a></p></td>
</tr>
<tr class="even">
<td><p>Enterprise Edition File Store</p></td>
<td><p><a href="lync-server-2013-restoring-a-file-store.md">Restoring a file store in Lync Server 2013</a></p></td>
</tr>
<tr class="odd">
<td><p>A standalone Monitoring database or Archiving database</p></td>
<td><p><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Restoring monitoring or archiving data in Lync Server 2013</a></p></td>
</tr>
<tr class="even">
<td><p>A stand-alone Persistent Chat database</p></td>
<td><p><a href="lync-server-2013-restoring-persistent-chat-data.md">Restoring Persistent Chat data in Lync Server 2013</a></p></td>
</tr>
</tbody>
</table>


## Gathering Hardware, Software, and Tools

When you restore a server, you need to start with a new or clean computer. Additionally, you must have the following hardware and software available:

  - A clean or new server with the same fully qualified domain name (FQDN) as the server that failed.
    

    > [!IMPORTANT]
    > When you install the operating system, make sure that you do not delete the computer account in Active Directory Domain Services, and verify that the group permissions for the account are retained.



  - Installation software for the operating system. To install the operating system, use the server deployment procedures and configurations established by your organization. You should have these procedures and configuration requirements available when you restore service.

  - Installation software for SQL Server 2012 or SQL Server 2008 R2. To install a database server, use the appropriate version of SQL Server and the database server deployment procedures and configurations established by your organization. You should have these procedures and configuration requirements available when you restore service.
    

    > [!NOTE]
    > The Lync Server Deployment Wizard automatically installs SQL Server 2012 Express on each Standard Edition server and on any other Lync Server server when a local configuration store is installed, unless you have preinstalled SQL Server 2012 or SQL Server 2008 R2 on the server.



  - Software for taking system images.
    

    > [!TIP]
    > We recommend that you take an image copy of the system after you install the operating system and SQL Server, and before you start restoration, so that you can use this image as a rollback point in case something goes wrong during restoration.



  - Lync Server 2013 installation software. The Lync Server Deployment Wizard is located in the Lync Server installation folder or media at \\setup\\amd64\\Setup.exe.

During restoration, you use the following tools:

  - Lync Server Management Shell cmdlets

  - Import-CsUserData

  - Tools for restoring Windows folders

  - Topology Builder

  - SQL Server database utilities, such as SQL Server Management Studio

## Preparing to Restore a Server

Before you restore the server, you must perform the following steps:

1.  Install the operating system.

2.  If the server is a Back End Server, install SQL Server 2012 or SQL Server 2008 R2.

3.  Restore or reenroll your certificates. For details about certificates, see "Additional Backup Requirements" in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).

4.  Take an image of the system before starting restoration to use as a rollback point, in case something goes wrong during restoration.


> [!NOTE]
> The Lync Server Deployment Wizard and cmdlets described in the procedures in this topic, and related topics, set all required access control lists (ACLs).



Verify that the hardware and the software that you need for the components that you plan to restore are available before you start restoration. After you install the operating system and SQL Server, most of the steps in the following restoration procedures can be run remotely. The exceptions are noted in the procedures.

You should also have your organization's backup and restoration plan and the information from your last backup, such as the information in the worksheets in this document (for details, see [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), available before you begin restoration.

