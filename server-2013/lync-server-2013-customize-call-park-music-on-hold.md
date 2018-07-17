---
title: 'Lync Server 2013: Customize Call Park music on hold'
TOCTitle: Customize Call Park music on hold
ms:assetid: 3d78e6f9-a4ae-49f4-a89f-4515acb49dac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688031(v=OCS.15)
ms:contentKeyID: 49733621
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Customize Call Park music on hold in Lync Server 2013

 


You can specify your own music file to use for music on hold, instead of the default music file that ships with Lync Server 2013. To customize music on hold, use the **Set-CsCallParkServiceMusicOnHoldFile** cmdlet.


> [!NOTE]
> If you customize music on hold and want the same music for multiple sites, you must configure the music file for each site that runs the Call Park application.



## To customize the music file

1.  Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

2.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

3.  Run:
    
        Set-CsCallParkServiceMusicOnHoldFile -Service <ServiceID where the Call Park application resides> -Content <Byte[]>
    

    > [!TIP]
    > Use the <STRONG>Get-CsService</STRONG> cmdlet to identify the service. For details, see <A href="https://technet.microsoft.com/en-us/library/gg413038(v=ocs.15)">Get-CsService</A>.

    
    The following example shows how to obtain the contents of a file, soothingmusic.wma, as a byte array and assign it to a variable. Then the audio file is assigned as the music-on-hold file for Call Park. For details, see [Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/en-us/library/gg412836\(v=ocs.15\)).
    
        $a = Get-Content -ReadCount 0 -Encoding byte "C:\MoHFiles\soothingmusic.wma"
        Set-CsCallParkServiceMusicOnHoldFile -Service Redmond1-applicationserver-1 -Content $a

## See Also


[Set-CsCallParkServiceMusicOnHoldFile](https://technet.microsoft.com/en-us/library/gg412836\(v=ocs.15\))  
[Get-CsService](https://technet.microsoft.com/en-us/library/gg413038\(v=ocs.15\))

