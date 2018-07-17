---
title: 'Lync Server 2013: Defining normalization rules'
TOCTitle: Defining normalization rules
ms:assetid: ed31d56c-00b5-4f72-bd9f-beb4100d441f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399071(v=OCS.15)
ms:contentKeyID: 48185741
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Defining normalization rules in Lync Server 2013

 


Lync Server 2013 normalization rules use .NET Framework regular expressions to translate dialed phone numbers to E.164 format; in other words, normalization rules take the phone number dialed by a user and convert that number to the format used internally by Lync Server. Each dial plan must be assigned one or more normalization rules.

For details about normalization rules, see [Dial plans and normalization rules in Lync Server 2013](lync-server-2013-dial-plans-and-normalization-rules.md) in the Planning documentation.

For details about how to write regular expressions, see ".NET Framework Regular Expressions" at [http://go.microsoft.com/fwlink/p/?linkId=140927](http://go.microsoft.com/fwlink/p/?linkid=140927).

You can use either of the following methods to define or edit a normalization rule:

  - Use the **Build a Normalization Rule** tool to specify values for the starting digits, length, digits to remove and digits to add, and then let Lync Server Control Panel generate the corresponding matching pattern and translation rule for you.

  - Write regular expressions manually to define the matching pattern and translation rule.

## In This Section

  - [Create or modify a normalization rule by using Build a Normalization Rule in Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-by-using-build-a-normalization-rule.md)

  - [Create or modify a normalization rule manually in Lync Server 2013](lync-server-2013-create-or-modify-a-normalization-rule-manually.md)

## See Also


[Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md)  
[Modify a dial plan in Lync Server 2013](lync-server-2013-modify-a-dial-plan.md)

