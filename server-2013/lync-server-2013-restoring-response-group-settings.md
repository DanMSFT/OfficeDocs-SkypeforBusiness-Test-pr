---
title: 'Lync Server 2013: Restoring Response Group settings'
TOCTitle: Restoring Response Group settings
ms:assetid: 4f8e1949-925d-4538-be1d-9ac7c06b2aca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202174(v=OCS.15)
ms:contentKeyID: 51541473
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Restoring Response Group settings in Lync Server 2013

 


If you deployed the Response Group application and you need to restore a Back End Server or a Standard Edition server, you also need to restore the Response Group configuration settings.

## To restore Response Group configuration settings

1.  At the command line, type:
    
        Import-CsRgsConfiguration -Destination "service:ApplicationServer:<pool FQDN>" -OverwriteOwner -FileName "<path and file name of the backed up file at $Backup>"
    
    For example:
    
        Import-CsRgsConfiguration -Destination "service: ApplicationServer:pool01.contoso.com" -OverwriteOwner -FileName "C:\RgsConfiguration.zip"

