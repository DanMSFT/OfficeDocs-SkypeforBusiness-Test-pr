---
title: 'Lync Server 2013: Assign policies to a common area phone'
TOCTitle: Assign policies to a common area phone
ms:assetid: f0554fd1-b237-49b3-9eb4-26f4b91f5604
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994082(v=OCS.15)
ms:contentKeyID: 51803993
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Assign policies in Lync Server 2013 to a common area phone

 


After you create your policy for common area phones (for details, see [Create a voice policy and configure PSTN usage records in Lync Server 2013](lync-server-2013-create-a-voice-policy-and-configure-pstn-usage-records.md)), you can assign the policy to a common area phone by using Windows PowerShell and the appropriate **Grant-Cs** cmdlet. These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell. For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [http://go.microsoft.com/fwlink/p/?linkId=255876](http://go.microsoft.com/fwlink/p/?linkid=255876).


## Assigning a Policy to a Single Common Area Phone

  - The following command assigns the per-user voice policy RedmondVoice to the common area phone that has the Identity Building 14 Lobby.
    
        Grant-CsVoicePolicy -Identity "Building 14 Lobby" -PolicyName "RedmondVoicePolicy"

## Assigning a Policy to Multiple Common Area Phones

  - In this example, the per-user voice policy RedmondVoice is assigned to all the common area phones configured for use in the organization.
    
        Get-CsCommonAreaPhone | Grant-CsVoicePolicy  -PolicyName "RedmondVoicePolicy"

For details, see the Help topics for the [Grant-CsVoicePolicy](https://technet.microsoft.com/en-us/library/gg398828\(v=ocs.15\)).

## See Also


[Get-CsCommonAreaPhone](https://technet.microsoft.com/en-us/library/gg412934\(v=ocs.15\))

