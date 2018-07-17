---
title: Import policies and settings
TOCTitle: Import policies and settings
ms:assetid: b25decee-2ee5-4836-b370-454411d39252
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205178(v=OCS.15)
ms:contentKeyID: 48185147
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Import policies and settings

 


After you merge your Office Communications Server 2007 R2 topology information with your Lync Server 2013 pilot pool, you need to run a Lync Server 2013 Management Shell cmdlet to migrate your Office Communications Server 2007 R2 policies and configuration settings to your Lync Server 2013 pilot pool.

The **Import-CsLegacyConfiguration** cmdlet imports policies, voice routes, dial plans, Communicator Web Access URLs, and dial-in access numbers to Lync Server 2013.

## To migrate policies and settings

1.  On the Lync Server 2013 Front End server, start the Lync Server Management Shell.

2.  At the command line, type the following:
    
        Import-CsLegacyConfiguration
    
    After the policies are imported, use the procedure that follows to see the imported policies in the Lync Server Control Panel .

## To view imported policies

1.  Open Lync Server 2013 Control Panel.

2.  Click **Voice Routing** and view the imported policies.

3.  Click **Conferencing** and view the imported policies.

4.  Click **Federation and External Access** and view the imported policies.

5.  Click **Monitoring and Archiving** and view the imported policies.

