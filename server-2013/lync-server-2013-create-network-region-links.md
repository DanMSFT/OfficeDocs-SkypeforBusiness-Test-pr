---
title: 'Lync Server 2013: Create network region links'
TOCTitle: Create network region links
ms:assetid: f8163910-8935-475d-88a2-3aa44feb9dbe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413047(v=OCS.15)
ms:contentKeyID: 48185873
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Create network region links in Lync Server 2013

 


Regions within a network are linked through physical WAN connectivity. A *network region link* creates a link between two regions configured for call admission control (CAC) and sets the bandwidth limitations on audio and video traffic between these regions.

For details about working with network region links, see the Lync Server Management Shell documentation for the following cmdlets:

  - [New-CsNetworkRegionLink](https://technet.microsoft.com/en-us/library/gg398437\(v=ocs.15\))

  - [Get-CsNetworkRegionLink](https://technet.microsoft.com/en-us/library/gg398972\(v=ocs.15\))

  - [Set-CsNetworkRegionLink](https://technet.microsoft.com/en-us/library/gg412867\(v=ocs.15\))

  - [Remove-CsNetworkRegionLink](https://technet.microsoft.com/en-us/library/gg413012\(v=ocs.15\))

The example topology has a link between the North America and APAC regions, and a link between the EMEA and APAC regions. Each of these region links is constrained by WAN bandwidth, as described in Region Link Bandwidth Information table in the [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) section of the Planning documentation.

## To create network region links by using Lync Server Management Shell

1.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

2.  Run the New-CsNetworkRegionLink cmdlet to create the region links and apply appropriate bandwidth policy profiles. For example, run:
    
        New-CsNetworkRegionLink -NetworkRegionLinkID NA-EMEA-LINK -NetworkRegionID1 NorthAmerica -NetworkRegionID2 EMEA -BWPolicyProfileID 50Mb_Link
    
        New-CsNetworkRegionLink -NetworkRegionLinkID EMEA-APAC-LINK -NetworkRegionID1 EMEA -NetworkRegionID2 APAC -BWPolicyProfileID 25Mb_Link

## To create network region links by using Lync Server Control Panel

1.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

2.  In the left navigation bar, click **Network Configuration**.

3.  Click the **Region Link** navigation button.

4.  Click **New**.

5.  On the **New Region Link** page, click **Name** and then type a name for the network region link.

6.  Click **Network Region \#1**, and then click the network region in the list that you want to link to Network Region \#2.

7.  Click **Network Region \#2**, and then click a network region in the list that you want to link to Network Region \#1.

8.  Optionally, click **Bandwidth policy**, and then select the bandwidth policy profile that you want to apply to the network region link.
    

    > [!NOTE]
    > Apply a bandwidth policy only if the network region link is bandwidth-constrained and you want to use CAC to control media traffic on that link.



9.  Click **Commit**.

10. To finish creating network region links for your topology, repeat steps 4 through 9 with settings for other regions.

