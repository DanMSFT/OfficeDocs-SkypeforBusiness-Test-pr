﻿---
title: 'Lync Server 2013: Remove Kerberos authentication from a site'
TOCTitle: Remove Kerberos authentication from a site
ms:assetid: 93171b02-bb36-42dc-943d-86d9dde45b59
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398749(v=OCS.15)
ms:contentKeyID: 48184806
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# In Lync Server 2013 remove Kerberos authentication from a site

 


To successfully complete this procedure you should be logged on as a user who is a member of the RTCUniversalServerAdmins group.

If you need to remove Kerberos authentication from a site or retire a site, you must remove the Kerberos authentication account assignment from the site by using the **Remove-CsKerberosAccountAssignment** cmdlet. Use the following procedure to remove the Kerberos authentication account assignment, which removes the assignment from all computers in the site.


> [!WARNING]
> If you are permanently retiring the Kerberos-enabled account, you should use Active Directory Users and Computers to delete it from Active Directory Domain Services after you have removed the assignment. If you plan to use the object in the future, you might want to keep the Active Directory object.



## To remove Kerberos authentication from a site

1.  As a member of the RTCUniversalServerAdmins group, log on to a computer in the domain running Lync Server 2013 or on to a computer where the administrative tools are installed.

2.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

3.  From the command line, run the following two commands:
    
        Remove-CsKerberosAccountAssignment -Identity "site:SiteName"
    
        Enable-CsTopology
    
    For example:
    
        Remove-CsKerberosAccountAssignment -Identity "site:Redmond"
    
        Enable-CsTopology
    

    > [!IMPORTANT]
    > After making any changes to Kerberos authentication, such as adding an account or removing an account, you must run <STRONG>Enable-CsTopology</STRONG> from the Lync Server Management Shell command prompt.


