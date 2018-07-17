---
title: 'Lync Server 2013: Deleting a message or purging obsolete messages'
TOCTitle: Deleting a message or purging obsolete messages
ms:assetid: 3f0c612d-6dfd-41a4-a5fe-5ff3448eb0ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215874(v=OCS.15)
ms:contentKeyID: 48706000
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Deleting a message or purging obsolete messages in Lync Server 2013

 


A Persistent Chat administrator can delete a message from a Persistent Chat room (and, optionally, can replace it with another message). Administrators can also purge obsolete messages as part of ongoing maintenance, to minimize growth of the database. For example, this Windows PowerShell command removes all the messages from the ITChatRoom chat room that were posted by the user kenmyer@litwareinc.com:

    Remove-CsPersistentChatMessage -Identity "atl-persistentchat-001.litwareinc.com\ITChatRoom" -UserUri "sip:kenmyer@litwareinc.com"

And this example replaces any removed messages with the note that the message is no longer available:

    Remove-CsPersistentChatMessage -Identity "atl-persistentchat-001.litwareinc.com\ITChatRoom" -UserUri "sip:kenmyer@litwareinc.com" -ReplaceMessage "This message is no longer available."

For more information, see the help topic for the [Remove-CsPersistentChatMessage](https://technet.microsoft.com/en-us/library/jj204668\(v=ocs.15\)) cmdlet.

