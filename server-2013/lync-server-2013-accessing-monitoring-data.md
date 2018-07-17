---
title: 'Lync Server 2013: Accessing monitoring data'
TOCTitle: Accessing monitoring data
ms:assetid: 845385ca-5532-4fa2-91b9-51c6de6fec91
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688116(v=OCS.15)
ms:contentKeyID: 49733714
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Accessing monitoring data in Lync Server 2013

 


Monitoring data is stored in a pair of SQL Server databases: LcsCdr for call detail recording data, and QoEMetrics for Quality of Experience data. There is nothing special about these two databases; that means that the data stored in those databases can be accessed using any of the tools you typically use for accessing and analyzing SQL Server data.

One tool you should consider for accessing and analyzing monitoring data is the Lync Server Monitoring Reports. Monitoring Reports are a set of standard reports that are published by Microsoft SQL Server Reporting Service. These reports, which are accessible by using a web browser, provide usage, call diagnostic information, and media quality information, all based on call detail recording (CDR) and Quality of Experience (QoE) records stored in the CDR and QoE databases. Monitoring Reports ship with Lync Server 2013 and can be installed from the Lync Server Deployment Wizard after Lync Server has been installed and monitoring has been configured.

As noted, Monitoring Reports requires the use of SQL Server Reporting Service. SQL Server Reporting Service can be installed at the same time you install SQL Server or can be installed any time after SQL Server itself has been installed.

For more information, see the topic [Installing Lync Server 2013 Monitoring Reports](lync-server-2013-installing-lync-server-2013-monitoring-reports.md) in the Lync Server 2013 deployment guide.

