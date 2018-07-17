---
title: 'Lync Server 2013: Delete an announcement'
TOCTitle: Delete an announcement
ms:assetid: 26ea7149-4470-4c22-9bab-8a4065aca44e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687998(v=OCS.15)
ms:contentKeyID: 49733588
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Delete an announcement in Lync Server 2013

 


Use the following procedure to delete an announcement that is used for calls to unassigned numbers.

## To delete an announcement

1.  Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

2.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

3.  List all the announcements in your organization. At the command line, run:
    
        Get-CsAnnouncement

4.  In the resulting list, locate the announcement you want to delete, and copy the GUID. Then, at the command line, run:
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>" 
    
    For example:
    
        Remove-CsAnnouncement -Identity "ApplicationServer:Redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"
    

    > [!NOTE]
    > For details about more options, see <A href="https://technet.microsoft.com/en-us/library/gg398937(v=ocs.15)">Get-CsAnnouncement</A> and <A href="https://technet.microsoft.com/en-us/library/gg412766(v=ocs.15)">Remove-CsAnnouncement</A>.



## See Also


[Create an announcement in Lync Server 2013](lync-server-2013-create-an-announcement.md)  


[Remove-CsAnnouncement](https://technet.microsoft.com/en-us/library/gg412766\(v=ocs.15\))  
[Get-CsAnnouncement](https://technet.microsoft.com/en-us/library/gg398937\(v=ocs.15\))

