---
title: Remove the SQL Server database for a Monitoring server
TOCTitle: Remove the SQL Server database for a Monitoring server
ms:assetid: aed5e394-d63e-4ad4-af40-f12d3a044344
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721848(v=OCS.15)
ms:contentKeyID: 49733781
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Remove the SQL Server database for a Monitoring server

 


After you remove a Microsoft Lync Server 2010 Monitoring Server, you can remove the SQL Server databases that hosted the server data. Use the following procedures to remove the definitions from Topology Builder, and then remove the database and log files from the database server.

## To remove the SQL Server database using Topology Builder

1.  On the Lync Server 2013 Front End Server, open Topology Builder.

2.  In Topology Builder, navigate to **Shared Components** and then **SQL Server Stores**, right-click the SQL Server instance associated with the removed or reconfigured Monitoring Server, and then click **Delete**.

3.  Publish the topology, and then check replication status.

## To remove the database files from the SQL Server

1.  To remove the databases on the SQL Server-based server, you must be a member of the SQL Server sysadmins group for the SQL Server server where you are removing the database files.

2.  Open the Lync Server Management Shell.

3.  At the command line, type the following:
    
        Uninstall-CsDataBase -DatabaseType Monitoring -SqlServerFqdn <FQDN> [-SqlInstanceName <instance>]
    
    Where \<FQDN\> is the fully qualified domain name (FQDN) of the database server, and \<instance\> is the optional named database instance.

4.  When the **Uninstall-CsDataBase** cmdlet prompts you to confirm actions, read the information, and then press **Y** (or press Enter) to proceed, or press **N** and then Enter if you want to stop the cmdlet (that is, in case there errors).

