﻿---
title: 'Lync Server 2013: Exporting and importing voice routing configuration'
TOCTitle: Exporting and importing voice routing configuration
ms:assetid: c9b78622-5725-43b0-9ee1-5b82b1e1c8eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398836(v=OCS.15)
ms:contentKeyID: 48185398
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Exporting and importing voice routing configuration in Lync Server 2013

 


If you want to save your voice routing configuration without publishing it, follow these steps to use the Lync Server Control Panel configuration export and import commands to save and retrieve a snapshot of your voice routing configuration. When you import a voice routing configuration file (.vcfg), but changes have been made to the voice routing configuration on the server in the meantime, the pages in the **Voice Routing** group in Lync Server Control Panel will indicate that there are uncommitted changes to voice routing. Those uncommitted changes are the differences between the two configurations that require reconciliation.


> [!IMPORTANT]
> If you have made any uncommitted changes to the settings on any page within the <STRONG>Voice Routing</STRONG> group, the changes are saved in the exported voice configuration file (.vcfg). This enables you to make voice routing configuration changes during multiple Lync Server Control Panel sessions before you publish the changes.



## In This Section

  - [Export a voice route configuration file in Lync Server 2013](lync-server-2013-export-a-voice-route-configuration-file.md)

  - [Import a voice route configuration file in Lync Server 2013](lync-server-2013-import-a-voice-route-configuration-file.md)

## Related Sections

