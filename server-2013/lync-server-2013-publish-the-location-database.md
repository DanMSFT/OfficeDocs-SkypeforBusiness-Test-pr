---
title: 'Lync Server 2013: Publish the location database'
TOCTitle: Publish the location database
ms:assetid: dd032b5b-df0e-4017-ac46-e17570c1ab1e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398974(v=OCS.15)
ms:contentKeyID: 48185598
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Publish the location database from Lync Server 2013

 


The new locations that you added to the location database will not be made available to the client until they have been published.

For details, see the Lync Server Management Shell documentation for the following cmdlet:

  - **Publish-CsLisConfiguration**

If you use Emergency Location Identification Number (ELIN) gateways, you also need to upload the ELINs to your public switched telephone network (PSTN) carrier's Automatic Location Identification (ALI) database. Your PSTN carrier may require you to use a specific format for the ELIN records. Contact your PSTN carrier for details. You can export the records from the Location Information service database and format them as required.

## To publish the location database

  - Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

  - Run the following cmdlet to publish the location database.
    
        Publish-CsLisConfiguration

