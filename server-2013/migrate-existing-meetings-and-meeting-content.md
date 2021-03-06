﻿---
title: Migrate existing meetings and meeting content
TOCTitle: Migrate existing meetings and meeting content
ms:assetid: 30516731-2ae1-4a6d-a7e1-d3f05778c954
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688011(v=OCS.15)
ms:contentKeyID: 49733599
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Migrate existing meetings and meeting content

 


When a user account is moved from Lync Server 2010 to a Lync Server 2013 server, the following information is moved with that user account:

  - **Meetings already scheduled by the user**. This includes moving the conferencing directories and conferencing data.

  - **User’s personal identification number (PIN)**. The user’s current PIN continues to work until it expires or the user requests a new PIN.

The following user account information does not move to the new server.

  - **Meeting content**. In order to move the content shared during a meeting, for example PowerPoint, Whiteboard, attachments or poll data, use the **-MoveConferenceData** parameter as part of the **Move-CsUser** cmdlet.

