---
title: 'Lync Server 2013: Configure Persistent Chat Server'
TOCTitle: Configure Persistent Chat Server
ms:assetid: 85028aff-a38e-4748-958e-59e707a47532
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205054(v=OCS.15)
ms:contentKeyID: 48184709
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Configure Persistent Chat Server in Lync Server 2013

 


To create a new Persistent Chat configuration

    New-CsPersistentChatConfiguration -Identity <XdsIdentity> [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

To get Persistent Chat configuration

    Get-CsPersistentChatConfiguration [-LocalStore <Switch Parameter>] [-Identity <XdsIdentity>]

To remove Persistent Chat configuration

    Remove-CsPersistentChatConfiguration -Identity <XdsIdentity>

To set Persistent Chat configuration

    Set-CsPersistentChatConfiguration [-DefaultChatHistory <Integer>] [-MaxChatContentSizeMB <Integer>] [-MaxFileSizeKB <Integer>] [-ParticipantUpdateLimit <Integer>] [-FileServiceUrl <UrlForFileUpload>] [-RoomManagementUrl <RoomManagementUrl>] [-Instance <PSObject >] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>] [-WhatIf <Switch Parameter>]

For Lync Server 2013, all web service traffic is supported on the Lync Server 2013, Front End Servers. Therefore, the gcweb01 address on Persistent Chat Server is not necessary. We still support internal web service access because we provide the File Upload/Download Web service to the *internal* website only (not to the *external* website for remote users).

