﻿---
title: 'Lync Server 2013: (Optional) Define Response Group holiday sets'
TOCTitle: (Optional) Define Response Group holiday sets
ms:assetid: 56c37b3b-6517-49b9-86b7-ae48cc349119
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688063(v=OCS.15)
ms:contentKeyID: 49733657
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# (Optional) Define Response Group holiday sets in Lync Server 2013

 


Holiday settings define the days that a response group is closed for business and specify the action to take on those days. A holiday set is the collection of holidays that apply to a response group.


> [!NOTE]
> If a workflow is defined as a Managed workflow, then any user is assigned the CsResponseGroupManager role can set and modify holidays for workflows that they manage.



## To create a holiday set

1.  Log on as a member of the RTCUniversalServerAdmins group, or as a member of one of the predefined administrative roles that support Response Group.

2.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

3.  For each holiday you want to define, run:
    
        $x = New-CsRgsHoliday [-Name <holiday name>] -StartDate <starting date of holiday> -EndDate <ending date of holiday>
    
    To create the holiday set that contains the holidays you defined, run:
    
        New-CsRgsHolidaySet -Parent <service where the workflow is hosted> -Name <unique name for holiday set> -HolidayList <one or more holidays to be included in the holiday set>
    
    The following example shows a holiday set that includes two holidays:
    
        $a = New-CsRgsHoliday -Name "New Year's Day" -StartDate "1/1/2013 12:00 AM" -EndDate "1/1/2013 12:00 AM" 
        $b = New-CsRgsHoliday -Name "Independence Day" -StartDate "7/4/2013 12:00 AM" -EndDate "7/5/2013 12:00 AM" 
        New-CsRgsHolidaySet -Parent "ApplicationServer:Redmond.contoso.com -Name "2013 Holidays" -HolidayList ($a, $b)

## See Also


[Create or modify a hunt group workflow in Lync Server 2013](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)  
[Create or modify an interactive workflow in Lync Server 2013](lync-server-2013-create-or-modify-an-interactive-workflow.md)  


[New-CsRgsHoliday](https://technet.microsoft.com/en-us/library/gg398075\(v=ocs.15\))  
[New-CsRgsHolidaySet](https://technet.microsoft.com/en-us/library/gg398403\(v=ocs.15\))

