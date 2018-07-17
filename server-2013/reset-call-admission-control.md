---
title: Reset call admission control
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Reset call admission control

 


If a Lync Server 2010 Front End pool is hosting call admission control (CAC), you must move CAC hosting to a Lync Server 2013 pool before you can remove the Lync Server 2010 Front End pool.

## To reset CAC

1.  Open Topology Builder.

2.  Right-click the site node, and then click **Edit Properties**.

3.  Under **Call Admission Control setting**, make sure **Enable Call Admission Control** is selected.

4.  Under **Front End pool to run call admission control (CAC)**, select the Lync Server 2013 pool that is to host CAC, and then click **OK**.

5.  Publish the topology.

