﻿---
title: 'Lync Server 2013: Create Response Group agent groups'
TOCTitle: Create Response Group agent groups
ms:assetid: 2a80de17-ead0-46e8-8a27-7a4e233dbde0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520969(v=OCS.15)
ms:contentKeyID: 48183688
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Create Response Group agent groups Lync Server 2013

 


When you create an agent group, you select the agents that are assigned to the group and specify additional group settings, such as the routing method and whether an agent can sign in to and out of the group.

An agent who must sign in and out of the group, which is different from signing in or out of Lync Server, is called a *formal agent*. Formal agents must be signed in to the group before they can receive calls routed to the group. This can be useful for agents who answer calls from the group on a part-time basis. Formal agents sign in and out of their groups by clicking a menu item in Lync 2013 to open the Windows Internet Explorer Internet browser and display a webpage console.

An agent who does not sign in or out of the group is called an *informal agent*. Informal agents are automatically signed in to the group when they sign in to Lync Server, and they cannot sign out of the group.


> [!NOTE]
> Only on-premises users can be agents. If an agent is moved from on-premises to online, Response Group calls will not be routed to that agent.



## In This Section

[Create or modify an agent group in Lync Server 2013](lync-server-2013-create-or-modify-an-agent-group.md)

