---
title: 'Lync Server 2013: System requirements for SQL Server'
TOCTitle: System requirements for SQL Server
ms:assetid: 9c235085-cbfa-4e9e-9cec-3f5749039a6b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205112(v=OCS.15)
ms:contentKeyID: 48184904
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# System requirements for SQL Server in Lync Server 2013

 


Before you deploy Enterprise Edition server, install Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 on a dedicated computer that meets the hardware requirements. For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation. For details about software requirements, see [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md) in the Supportability documentation. For information about the permissions necessary for deployment, see [Deployment permissions for SQL Server in Lync Server 2013](lync-server-2013-deployment-permissions-for-sql-server.md).

Before you create the Front End pool, you must also configure Windows Firewall to allow Lync Server 2013 access to SQL Server over specific ports by defining ports for the server using SQL Server Configuration Manager and opening ports in Windows Firewall with Advanced Security.

