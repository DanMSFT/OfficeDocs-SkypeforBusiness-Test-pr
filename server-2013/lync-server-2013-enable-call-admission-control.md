---
title: 'Lync Server 2013: Enable call admission control'
TOCTitle: Enable call admission control
ms:assetid: 80201105-18f7-4c02-9c71-8df5a952f6c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398642(v=OCS.15)
ms:contentKeyID: 48184650
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Enable call admission control in Lync Server 2013

 


After you have configured your network settings for call admission control deployment, you must enable CAC to put your bandwidth policies into effect.

For details, see the Lync Server Management Shell documentation for the following cmdlets:

  - [Get-CsNetworkConfiguration](https://technet.microsoft.com/en-us/library/gg398140\(v=ocs.15\))

  - [Set-CsNetworkConfiguration](https://technet.microsoft.com/en-us/library/gg398927\(v=ocs.15\))

  - [Remove-CsNetworkConfiguration](https://technet.microsoft.com/en-us/library/gg398938\(v=ocs.15\))

## To enable call admission control by using Management Shell

1.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

2.  Run the Set-CsNetworkConfiguration cmdlet to enable CAC in your network. For example, run:
    
        Set-CsNetworkConfiguration -EnableBandwidthPolicyCheck 1
    
    If you want to disable CAC in your network, run the following:
    
        Set-CsNetworkConfiguration -EnableBandwidthPolicyCheck 0

## To enable call admission control by using Lync Server Control Panel

1.  Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel. For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).

2.  In the left navigation bar, click **Network Configuration**.

3.  Click the **Global** navigation button.

4.  Click **Global** in the list, and then select **Show Details** on the **Edit** menu.

5.  On the **Edit Global Settings** page, select the **Enable call admission control** check box.
    

    > [!NOTE]
    > If you want to disable call admission control throughout your deployment, clear this check box.



6.  Click **Commit**.

