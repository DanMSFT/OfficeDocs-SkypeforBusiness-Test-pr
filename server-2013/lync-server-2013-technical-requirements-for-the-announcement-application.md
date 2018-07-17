---
title: 'Lync Server 2013: Technical requirements for the Announcement application'
TOCTitle: Technical requirements for the Announcement application
ms:assetid: fbd8c204-3765-4b22-a0c9-a781b5126366
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205413(v=OCS.15)
ms:contentKeyID: 48185944
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Technical requirements for the Announcement application in Lync Server 2013

 


This section describes the following technical requirements for the Announcement application:

  - Hardware requirements

  - Software requirements

  - Port requirements

  - Audio file requirements

## Hardware Requirements

The Announcement application has the same hardware requirements as Front End Servers. For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.

## Software Requirements

The Announcement application has the same operating system requirements and software prerequisites as Front End Servers. For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.

All Front End Servers or Standard Edition servers that run the Announcement application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2. For Windows Server 2008 R2, the Windows Media Format Runtime is installed as part of Windows Desktop Experience. Windows Media Format Runtime or Microsoft Media Foundation is required for Windows Media Audio (.wma) files that the Announcement application plays for announcements and music.

## Port Requirements

The Announcement application uses the following port:

  - **Port 5071**   Used for SIP listening requests


> [!NOTE]
> This port is the default setting, which you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet. For details about this cmdlet, see the Lync Server Management Shell documentation.



## Audio File Requirements

The Announcement application supports Wave (.wav) file format and Windows Media audio (.wma) file format for music and announcements. Audio file requirements for the Announcement application are the same as for the Response Group application. For details, see [Technical requirements for Response Group in Lync Server 2013](lync-server-2013-technical-requirements-for-response-group.md).

