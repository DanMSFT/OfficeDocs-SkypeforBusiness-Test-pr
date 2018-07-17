---
title: 'Lync Server 2013: Requirements for running Best Practices Analyzer'
TOCTitle: Requirements for running Best Practices Analyzer
ms:assetid: 3c7dc44e-5f8a-40a7-9ebb-9ad707ac0007
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg591345(v=OCS.15)
ms:contentKeyID: 48183880
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Requirements for running Best Practices Analyzer in Lync Server 2013

 


You can use Lync Server 2013, Best Practices Analyzer to scan your Lync Server 2013 environment. You cannot use it to scan previous environments, but you can use the previous versions of the tool to scan those environments. For details about downloading and using the Lync Server 2010 and Office Communications Server 2007 R2 versions of Best Practices Analyzer, see "Lync Server 2010, Best Practices Analyzer" at [http://go.microsoft.com/fwlink/p/?linkId=210536](http://go.microsoft.com/fwlink/p/?linkid=256358) and "Best Practices Analyzer for Office Communications Server 2007 and Office Communications Server 2007 R2" at [http://go.microsoft.com/fwlink/p/?linkId=256358](http://go.microsoft.com/fwlink/p/?linkid=210651).

Prior to starting your scan, you should ensure that all components in your Lync Server 2013 environment are running and online.


> [!NOTE]
> Depending on the configuration of your Edge Servers and any related perimeter network settings, including firewall settings and permissions, Best Practices Analyzer might not be able to access and scan your Edge Servers. If you include Edge Servers in your scan and the reports indicate that there is an issue with accessing Edge Servers, you might want to remove Edge Servers from the scan options and run the scan again so that the issues do not show up in the report.


