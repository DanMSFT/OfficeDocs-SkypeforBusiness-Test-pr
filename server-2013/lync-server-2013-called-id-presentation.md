---
title: 'Lync Server 2013: Called ID presentation'
TOCTitle: Called ID presentation
ms:assetid: cf6c6af5-3418-411e-a50b-7a9cf8e100d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721892(v=OCS.15)
ms:contentKeyID: 49733826
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Called ID presentation in Lync Server 2013

 


With Lync Server 2010, the called party’s phone number (that is, the phone number called) can be translated from E.164 format to the local dialing format that is required by the trunk peer (that is, the associated gateway, private branch exchange (PBX), or SIP trunk). To do this, you must define one or more translation rules to translate the Request URI before routing it to the trunk peer.


> [!IMPORTANT]
> The ability to associate one or more translation rules with an Enterprise Voice trunk configuration is intended to be used as an <EM>alternative</EM> to configuring translation rules on the trunk peer. Do not associate translation rules with an Enterprise Voice trunk configuration if you have configured translation rules on the trunk peer because the two rules might conflict.



You can use either of the following methods to create or modify a translation rule:

  - Use the **Build a Translation Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.

  - Write regular expressions manually to define the matching pattern and translation rule.


> [!NOTE]
> For information about how to write regular expressions, see ".NET Framework Regular Expressions" at <A href="http://go.microsoft.com/fwlink/p/?linkid=140927">http://go.microsoft.com/fwlink/p/?linkId=140927</A>.



## In This Section

  - [Create or modify a translation rule by using the Build a Translation Rule tool in Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-by-using-the-build-a-translation-rule-tool.md)

  - [Create or modify a translation rule manually in Lync Server 2013](lync-server-2013-create-or-modify-a-translation-rule-manually.md)

## See Also


[Caller ID presentation in Lync Server 2013](lync-server-2013-caller-id-presentation.md)

