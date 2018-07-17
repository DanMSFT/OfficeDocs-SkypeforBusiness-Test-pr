---
title: 'Lync Server 2013: Using cmdlets to reverse forest preparation'
TOCTitle: Using cmdlets to reverse forest preparation
ms:assetid: f48c7eb3-ccb0-48e6-ac79-ab7c7062b9d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413024(v=OCS.15)
ms:contentKeyID: 48185822
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Using cmdlets to reverse forest preparation for Lync Server 2013

 


Use the **Disable-CsAdForest** cmdlet to reverse the forest preparation step.


> [!WARNING]
> If you run the <STRONG>Disable-CsAdForest</STRONG> cmdlet in an environment where you also have a previous version of Lync Server deployed, the global settings for the previous version will also be deleted.



## To use cmdlets to reverse forest preparation

1.  Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.

2.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

3.  Run:
    
        Disable-CsAdForest [-Force] [-GroupDomain <FQDN of the domain in which universal groups were created>]
    
    For example:
    
        Disable-CsAdForest -Force -GroupDomain contoso.net
    
    The Force parameter specifies whether to force running the task. If this parameter is not present, the command will not run if even one domain in the forest is still prepared for Lync Server 2013. If the Force parameter is specified, the action will continue regardless of the state of other domains in the forest.
    
    If you do not specify the GroupDomain parameter, the default value is the local domain.

## See Also


[Running forest preparation for Lync Server 2013](lync-server-2013-running-forest-preparation.md)  


[Preparing the forest for Lync Server 2013](lync-server-2013-preparing-the-forest.md)

