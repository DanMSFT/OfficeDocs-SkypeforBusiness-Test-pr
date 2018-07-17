---
title: Migrate analog devices
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Migrate analog devices

 


Lync Server provides support for analog devices. Specifically, the supported analog devices are analog audio phones and analog fax machines. You can configure the qualified gateways to support the use of analog devices in your Lync Server environment. After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices. Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.

## To migrate analog devices

1.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

2.  At the command line, type:
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  Verify that all contact objects have been moved to the Lync Server 2013 pool. At the command line, type:
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  Verify that all the contact objects are now associated with the Lync Server 2013 pool.

