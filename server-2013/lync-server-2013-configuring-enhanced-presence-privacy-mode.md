﻿---
title: 'Lync Server 2013: Configuring enhanced presence privacy mode'
TOCTitle: Configuring enhanced presence privacy mode
ms:assetid: e7a6b873-486d-4dfb-a967-c48f61f237f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399028(v=OCS.15)
ms:contentKeyID: 48185664
ms.date: 12/09/2014
mtps_version: v=OCS.15
---

# Configuring enhanced presence privacy mode in Lync Server 2013

 


With enhanced presence privacy mode, users can restrict their presence information so that it is visible only to the contacts listed in their Lync 2013 Contacts list. The **New-CsPrivacyConfiguration** and **Set-CsPrivacyConfiguration** cmdlets have an EnablePrivacyMode parameter controls this option. When EnablePrivacyMode is set to True, the option to restrict presence information to contacts becomes available in the Lync 2013 Status options. When EnablePrivacyMode is set to False, users can choose either to always allow everyone to see their presence information or to adhere to any future changes the administrator makes to the privacy mode.


> [!IMPORTANT]
> Lync 2013 and Lync 2010 privacy settings are not honored by previous versions (Microsoft Office Communicator 2007 R2 or Microsoft Office Communicator 2007). If previous versions of Office Communicator are allowed to sign in, a Lync 2013 user’s status, contact information, or picture could be viewed by someone who has not been authorized to view it. Additionally, a Lync 2013 user’s privacy settings are reset if he or she later signs in with previous version of Communicator.<BR>For these reasons, in a migration scenario, before you enable enhanced presence privacy mode: 
> <UL>
> <LI>
> <P>Ensure that every user has Lync 2013 installed.</P>
> <LI>
> <P>Define a client version policy rule to prevent previous versions of Communicator from signing in.</P></LI></UL>



## To enable enhanced presence privacy mode

1.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

2.  Run the following command:
    
        Get-CsPrivacyConfiguration | Set-CsPrivacyConfiguration -EnablePrivacyMode $True
    
    This command enables privacy mode for all the privacy configuration settings currently in use in the organization. For more information about how the Lync Server enhanced presence privacy mode policy configurations manages contact presence for the Lync 2013 client, see the Microsoft KB article [Enabling Lync Server enhanced presence privacy mode updates the presence status of some Lync contacts to "unavailable"](http://support.microsoft.com/kb/3020057).

## See Also


[Get-CsPrivacyConfiguration](https://technet.microsoft.com/en-us/library/gg413002\(v=ocs.15\))  
[New-CsPrivacyConfiguration](https://technet.microsoft.com/en-us/library/gg398807\(v=ocs.15\))  
[Set-CsPrivacyConfiguration](https://technet.microsoft.com/en-us/library/gg398484\(v=ocs.15\))

