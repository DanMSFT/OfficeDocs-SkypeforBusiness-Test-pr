﻿---
title: Remove the SQL Server database for an Archiving server
TOCTitle: Remove the SQL Server database for an Archiving server
ms:assetid: 6e8a1fcd-ed09-43b0-82c9-60e7ce116a01
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688087(v=OCS.15)
ms:contentKeyID: 49733686
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Remove the SQL Server database for an Archiving server

 


After you remove a Microsoft Lync Server 2010 Archiving Server, you can remove the SQL Server databases that hosted the pool data. Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.

## To remove the SQL Server database using Topology Builder

1.  On the Lync Server 2013 Front End Server, open Topology Builder.

2.  In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Archiving Server, and then click **Delete**.

3.  Publish the topology, and then check replication status.

## To remove the database files from the SQL Server

1.  To remove the databases on the SQL Server, you must be a member of the SQL Server sysadmins group for the SQL Server where you are removing the database files.

2.  Open the Lync Server Management Shell.

3.  At the command line, type the following:
    
        Uninstall-CsDataBase -DatabaseType Archiving -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the named database instance (that is, if one was defined).

4.  When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).

