---
title: 'Lync Server 2013: Create network intersite policies'
TOCTitle: Create network intersite policies
ms:assetid: b0714aae-55dc-4587-b718-34a03f596b22
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412844(v=OCS.15)
ms:contentKeyID: 48185148
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Create network intersite policies in Lync Server 2013

 


A *network intersite policy* defines bandwidth limitations between sites that have direct WAN links between them.

For details, see the Lync Server Management Shell documentation for the following cmdlets:

  - [New-CsNetworkInterSitePolicy](https://technet.microsoft.com/en-us/library/gg398994\(v=ocs.15\))

  - [Get-CsNetworkInterSitePolicy](https://technet.microsoft.com/en-us/library/gg412769\(v=ocs.15\))

  - [Set-CsNetworkInterSitePolicy](https://technet.microsoft.com/en-us/library/gg398772\(v=ocs.15\))

  - [Remove-CsNetworkInterSitePolicy](https://technet.microsoft.com/en-us/library/gg398963\(v=ocs.15\))


> [!IMPORTANT]
> A network intersite policy is required <EM>only</EM> if there is a direct cross link between two network sites.



In the example topology North America region, there is a direct link between the Reno and Albuquerque sites. These two sites require an intersite policy that applies an appropriate bandwidth policy profile. The following example applies the 20Mb\_Link profile.

## To create a network intersite policy

1.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

2.  Run the New-CsNetworkInterSitePolicy cmdlet to create network intersite policies and apply an appropriate bandwidth policy profile for two sites that have a direct cross link. For example, run:
    
        New-CsNetworkInterSitePolicy -InterNetworkSitePolicyID Reno_Albuquerque -NetworkSiteID1 Reno -NetworkSiteID2 Albuquerque -BWPolicyProfileID 20Mb_Link

3.  Repeat step 2 as needed to create network intersite policies for all network sites pairs that have a direct cross link.

