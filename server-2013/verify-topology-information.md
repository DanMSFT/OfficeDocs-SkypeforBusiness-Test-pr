---
title: Verify topology information
TOCTitle: Verify topology information
ms:assetid: aa4c424e-f87c-4be6-8df6-a0cd193b11fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205151(v=OCS.15)
ms:contentKeyID: 48185046
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Verify topology information

 


The first step in verifying the merge completed successfully is to view the Office Communications Server 2007 R2 topology information that you merged with Lync Server 2013. In Topology Builder, the **BackCompatSite** node displays the fully qualified domain name (FQDN) of each Office Communications Server 2007 R2 pool and server that you merged.

## To view BackCompatSite in Topology Builder

1.  In your Office Communications Server 2007 R2 environment, open the Office Communications Server 2007 R2 administrative tool and note the FQDNs of the legacy pools and servers.

2.  In your Lync Server 2013 environment, open Topology Builder and then expand the **BackCompatSite** node.

3.  Verify that the FQDNs for the pools and servers that you merge are displayed.
    

    > [!NOTE]
    > You do not see any information in <STRONG>BackCompatSite</STRONG> for server roles that are collocated on a Front End Server or Standard Edition server. Only server roles that are required for interoperability between Office Communications Server 2007 R2 and Lync Server 2013 are shown.



![Topology Builder BackCompatSite dialog box](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder BackCompatSite dialog box")

You can also use Lync Server 2013 Control Panel to view your merged topology. In Lync Server 2013 Control Panel, you can see each server FQDN, pool FQDN, and site name for your merged topology. Merged servers have a **Site** name of **BackCompatSite**.

## To view the merged topology in Lync Server 2013 Control Panel

1.  Open Lync Server 2013 Control Panel.

2.  Click **Topology**.

3.  On the **Status** tab, verify that servers and pools you merged appear by looking for **BackCompatSite** in the **Site** column.

![Lync Server Control Panel showing merged topology](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Lync Server Control Panel showing merged topology")

To see more detail about a merged pool, use the **Get-CsPool** cmdlet. In addition to the information that is available in Topology Builder and Lync Server 2013 Control Panel, this cmdlet displays the services that run on the Lync Server 2013 pool.


> [!NOTE]
> When you publish the topology after running the Merge wizard in Topology Builder, conference directories are merged to Lync Server 2013. Conference directories can be verified by running the <STRONG>Get-CsConferenceDirectory</STRONG> cmdlet.



## To view services on a merged pool

1.  Open the Lync Server 2013 Management Shell.

2.  At the command line, type the following:
    
        Get-CsPool [-Identity <FQDN of the pool>]
    
    For example:
    
        Get-CsPool -Identity pool02.contoso.net

## To verify conference directories merged

1.  Open the Lync Server 2013 Management Shell.

2.  At the command line, type the following:
    
        Get-CsConferenceDirectory

3.  Verify that all the conference directories for the pool or server you are merging are now in Lync Server 2013.

