---
title: 'Lync Server 2013: Disable Group Call Pickup for users'
TOCTitle: Disable Group Call Pickup for users
ms:assetid: 91b06f9e-2840-45a2-bbb3-6a29179b9a9f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945638(v=OCS.15)
ms:contentKeyID: 51541492
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Disable Group Call Pickup for users in Lync Server 2013

 


Use the following procedure to disable Group Call Pickup for a user.


> [!NOTE]
> When you disable Group Call Pickup for a user, the call pickup group number that was assigned to the user is not retained. If you subsequently want to re-enable Group Call Pickup for that user, you must assign the call pickup group number again with the /enablegrouppickup parameter.



## To disable Group Call Pickup for a user

1.  Log on to the computer where you installed the SEFAUtil tool with administrator rights.

2.  At the command line, run:
    
        SEFAUtil.exe sip:<sip address of user> /server:<pool FQDN> /disablegrouppickup
    
    For example:
    
        SEFAUtil.exe katarina@contoso.com /server:pool01.contoso.com /disablegrouppickup

## See Also


[Assign Group Call Pickup numbers to users in Lync Server 2013](lync-server-2013-assign-group-call-pickup-numbers-to-users.md)  
[Enable Group Call Pickup for users in Lync Server 2013](lync-server-2013-enable-group-call-pickup-for-users.md)

