﻿---
title: 'Lync Server 2013: Create an announcement'
TOCTitle: Create an announcement
ms:assetid: a6fd5922-fe46-41ba-94e3-c76b1101a31b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412783(v=OCS.15)
ms:contentKeyID: 48185005
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Create an announcement in Lync Server 2013

 


To create a new announcement, you need to perform the following steps:

1.  For audio prompts, record the audio file by using your favorite audio recording application.

2.  For audio prompts, run the **Import-CsAnnouncementFile** cmdlet to import the contents of the audio file to File Store.

3.  Run the **New-CsAnnouncement** cmdlet to create and name the announcement. Perform this step to create announcements with an audio prompt, a text-to-speech (TTS) prompt, or no prompt.
    

    > [!TIP]
    > You might want to create an announcement with no prompt (for example, if you want to transfer calls to a specific destination without playing a message).



4.  Assign the new announcement to a number range in the unassigned number table.

This topic describes how to import and create announcements. For details about assigning announcements in the unassigned number table, see [Configure the unassigned number table in Lync Server 2013](lync-server-2013-configure-the-unassigned-number-table.md).

## To create a new announcement

1.  For audio prompts, create the audio file.

2.  Log on to the computer where Lync Server Management Shell is installed as a member of the RTCUniversalServerAdmins group or with the necessary user rights as described in [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).

3.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

4.  For audio prompts, run:
    
        Import-CsAnnouncementFile -Parent <service of the Application Server running the Announcement application> -FileName <name for file in File Store> -Content Byte [<contents of file in byte array>]

5.  Run:
    
        New-CsAnnouncement -Parent <service of Application Server running the Announcement application, in the form: service:ApplicationServer:<fqdn>> -Name <unique name to be used as destination in unassigned number table> [-AudioFilePrompt <FileName specified in Import-CsAnnouncementFile>] [-TextToSpeechPrompt <text string to be converted to speech>] [-Language <Language for playing the TTS prompt (required for PromptTts)>] [-TargetUri sip:SIPAddress for transferring caller after announcement]
    
    For transferring calls to voice mail, type SIPAddress in the format sip:username@domainname;opaque=app:voicemail (for example, sip:bob@contoso.com;opaque=app:voicemail). For transferring calls to a phone number, type SIPAddress in the format sip:number@domainname;user=phone (for example, sip:+ 14255550121@contoso.com;user=phone).
    
    For example, to specify an audio prompt:
    
        $a = Get-Content ".\PromptFile.wav" -ReadCount 0 -Encoding Byte
        Import-CsAnnouncementFile -Parent service:ApplicationServer:pool0@contoso.com -FileName "ChangedNumberMessage.wav" -Content $a
        New-CsAnnouncement -Parent service:ApplicationServer:pool0.contoso.com -Name "Number Changed Announcement" -AudioFilePrompt "ChangedNumberMessage.wav"
    
    For example, to specify a TTS prompt:
    
        New-CsAnnouncement -Parent service:ApplicationServer:pool0.contoso.com -Name "Help Desk Announcement" -TextToSpeechPrompt "The Help Desk number has changed. Please dial 5550100." -Language "en-US"
    
    For more detail about these cmdlets, and to see a list of the language codes to use in the **TextToSpeechPrompt** parameter, see [New-CsAnnouncement](https://technet.microsoft.com/en-us/library/gg398522\(v=ocs.15\)).

## See Also


[Import-CsAnnouncementFile](https://technet.microsoft.com/en-us/library/gg398472\(v=ocs.15\))  
[New-CsAnnouncement](https://technet.microsoft.com/en-us/library/gg398522\(v=ocs.15\))  
[Configure the unassigned number table in Lync Server 2013](lync-server-2013-configure-the-unassigned-number-table.md)

