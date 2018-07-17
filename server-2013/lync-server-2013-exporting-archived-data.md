﻿---
title: 'Lync Server 2013: Exporting archived data'
TOCTitle: Exporting archived data
ms:assetid: 09450d54-769b-4741-924b-e390664d506f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204657(v=OCS.15)
ms:contentKeyID: 48183347
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Exporting archived data from Lync Server 2013

 


Data archived in Archiving databases is not searchable or in a readable format, but you can use the Export-CsArchivingData cmdlet to extract records from the database and save them as an Outlook Electronic Mail (EML) file. For details about exporting archived data, see [Export-CsArchivingData](https://technet.microsoft.com/en-us/library/gg398452\(v=ocs.15\)) in the Operations documentation.

If you enable Microsoft Exchange integration, data is archived in Exchange 2013 stores. Data archived in Exchange 2013 is searchable and discoverable. For details about support for integrated communications for Exchange 2013 and Lync Server 2013, see [Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md) in the Supportability documentation. For details about accessing data that is archived in Exchange, see the Exchange 2013 documentation.

## Exporting Archiving Data by Using Windows PowerShell Cmdlets

Archiving data can be exported by using the Export-CSArchivingData cmdlet. This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell. For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [http://go.microsoft.com/fwlink/p/?linkId=255876](http://go.microsoft.com/fwlink/p/?linkid=255876).

**To export archiving data**

  - This command exports all the archiving data written to the archiving database atl-sql-001.litwareinc.com since June 1, 2012. The resulting output file will be stored in the folder C:\\ArchivingExports.
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports"

**To export archiving data for a single user**

  - The following command exports archiving data for a single user: kenmyer@litwareinc.com. This is done by including the UserUri parameter followed by the user’s SIP address. For example:
    
        Export-CsArchivingData -Identity "ArchivingDatabase:atl-sql-001.litwareinc.com" -StartDate 6/1/2012 -OutputFolder "C:\ArchivingExports" -UserUri "sip:kenmyer@litwareinc.com"

For more information, see the help topic for the [Export-CsArchivingData](https://technet.microsoft.com/en-us/library/gg398452\(v=ocs.15\)) cmdlet.

## See Also


[Exchange Server and SharePoint integration support in Lync Server 2013](lync-server-2013-exchange-and-sharepoint-integration-support.md)  


[Export-CsArchivingData](https://technet.microsoft.com/en-us/library/gg398452\(v=ocs.15\))  
[Managing Lync Server 2013 Archiving](lync-server-2013-managing-archiving.md)

