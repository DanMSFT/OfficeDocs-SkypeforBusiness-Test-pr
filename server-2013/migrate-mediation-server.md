﻿---
title: Migrate Mediation Server
TOCTitle: Migrate Mediation Server
ms:assetid: b0b77121-2c8f-413e-b276-dbf1038361d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205173(v=OCS.15)
ms:contentKeyID: 48185117
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Migrate Mediation Server

 


Your Mediation Server is merged into your Lync Server 2013 pilot topology when you run the Merge wizard. You configure the Lync Server 2013 Mediation Server, however, after all users are migrated because an Office Communications Server 2007 R2 pool cannot communicate with a Lync Server 2013 Mediation Server. During the side-by-side migration, the Lync Server 2013 pool communicates with the Office Communications Server 2007 R2 Mediation Server.

When you configure your Lync Server 2013 Mediation Server, you must also upgrade or replace your Office Communications Server 2007 R2 gateways. Office Communications Server 2007 R2 gateways do not support Lync Server 2013 Mediation Server. You need to deploy gateways that are certified for Lync Server 2013 and associate them with the Lync Server 2013 Mediation Server. This step is required before you can completely decommission your Office Communications Server 2007 R2 deployment.

The topics in this section describe configuration tasks that you need to perform after you have completed your migration of Lync Server 2013 Mediation Server. Transitioning the collocated Mediation Server to a stand-alone Mediation Server is an optional task.

  - [Configure Mediation Server](configure-mediation-server.md)

  - [Change voice routes to use the new Lync Server 2013 Mediation Server](change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md)

  - [Transition a collocated Mediation Server to a stand-alone Mediation Server (optional)](transition-a-collocated-mediation-server-to-a-stand-alone-mediation-server-optional.md)

