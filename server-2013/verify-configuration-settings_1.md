﻿---
title: Verify configuration settings
TOCTitle: Verify configuration settings
ms:assetid: 41dbf91c-f2e1-4b9a-88cf-959575558cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204848(v=OCS.15)
ms:contentKeyID: 48183997
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Verify configuration settings

 


After you merge the topology and run the **Import-CsLegacyConfiguration** cmdlet, verify that your Office Communications Server 2007 R2 policies and settings were imported to Lync Server 2013. The following table lists the policies and settings that you should verify.

## Policies and Settings to Verify after Migration


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>If you use this workload:</th>
<th>Verify these policies and settings:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Instant messaging (IM) and conferencing</p></td>
<td><p>Presence policy</p>
<p>Conferencing policy</p></td>
</tr>
<tr class="even">
<td><p>Dial-in conferencing</p></td>
<td><p>Dial-in access numbers</p>
<p>Dial plans</p></td>
</tr>
<tr class="odd">
<td><p>Enterprise Voice</p></td>
<td><p>Voice policy</p>
<p>Voice routes</p>
<p>Dial plans</p>
<p>PSTN usage settings</p></td>
</tr>
<tr class="even">
<td><p>Communicator Web Access</p></td>
<td><p>Simple URLs</p></td>
</tr>
<tr class="odd">
<td><p>External users</p></td>
<td><p>External access policies</p></td>
</tr>
<tr class="even">
<td><p>Archiving</p></td>
<td><p>Archiving policy</p></td>
</tr>
</tbody>
</table>


## To verify policies and settings

1.  In your Office Communications Server 2007 R2 environment, make note of the names of dial plans (formerly known as location profiles), dial-in access numbers (Conferencing Attendant access phone numbers and regions), voice routes, and the policies listed in the preceding table, in addition to the URLs used for Communicator Web Access.

2.  On the Lync Server 2013 Front End server, open Lync Server Control Panel.

3.  To verify imported conferencing policies, in the left pane, click **Conferencing**, click **Conferencing Policy**, and then verify that all the conferencing policies in your Office Communications Server 2007 R2 environment are included in the list.
    

    > [!NOTE]
    > The <STRONG>Meeting</STRONG> policy from previous versions of Office Communications Server is now known as the conferencing policy in Lync Server 2013. Additionally, the <STRONG>Anonymous Particpants</STRONG> setting from previous versions of Office Communications Server is now a setting in the Lync Server 2013 conferencing policy.

    

    > [!NOTE]
    > In Office Communications Server 2007 R2, if the conferencing policy is not set to <STRONG>use per user</STRONG>, only global policy settings are imported. No other conference policies are imported in this situation.

    

    > [!NOTE]
    > If <STRONG>Anonymous Participants</STRONG> is set to <STRONG>Enforce per user</STRONG> in your Office Communications Server 2007 R2 conferencing policy, two conferencing policies are created during migration: one with <STRONG>AllowAnonymousParticipantsInMeetings</STRONG> set to <STRONG>True</STRONG> and one with <STRONG>AllowAnonymousParticipantsInMeetings</STRONG> set to <STRONG>False</STRONG>.



4.  To verify imported dial plans, click **Voice Routing**, click **Dial Plan**, and then verify that all the dial plans in your Office Communicator 2007 R2 environment are included in the list.
    

    > [!NOTE]
    > In Lync Server 2013, <STRONG>location profiles</STRONG> are now referred to as <STRONG>dial-plans</STRONG>.



5.  To verify imported voice policies, click **Voice Routing**, click **Voice Policy**, and then verify that all the voice policies in your Office Communicator 2007 R2 environment are included in the list.
    

    > [!NOTE]
    > If voice policy is not set to <STRONG>use per user</STRONG> in your Office Communications Server 2007 R2 environment, only global policy settings are imported. No other voice policies are imported in this situation.



6.  To verify imported voice routes, click **Voice Routing**, click **Route**, and then verify that all the voice routes in your Office Communicator 2007 R2 environment are included in the list.

7.  To verify imported PSTN usage settings, click **Voice Routing**, click **PSTN Usage**, and then verify that the PSTN Usage settings from your Office Communicator 2007 R2 environment are included in the list.

8.  To verify imported external access policies, click **Federation and External Access**, click **External Access Policy**, and then verify that all the external access policies in your Office Communicator 2007 R2 environment are included in the list.

9.  To verify archiving policies, click **Monitoring and Archiving**, click **Archiving Policy**, and then verify that all the archiving policies in your Office Communications Server 2007 R2 environment are included in the list.

10. Open the Lync Server Management Shell.

11. To verify presence policies, at the command line, type the following:
    
        Get-CsPresencePolicy
    
    By looking at the name in the **Identity** parameter, verify that all the presence policies in your Office Communications Server 2007 R2 environment were imported.

## To verify policies and settings by using cmdlets

1.  Open the Lync Server Management Shell.

2.  Run the cmdlets in the following table to verify policies and settings.
    
    The syntax of these cmdlets is like the following example:
    
        Get-CsConferencingPolicy
    
    For details about these cmdlets, run:
    
        Get-Help <cmdlet name> -Detailed


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>For this policy or setting:</th>
<th>Use this cmdlet:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Presence policy</p></td>
<td><p><strong>Get-CsPresencePolicy</strong></p></td>
</tr>
<tr class="even">
<td><p>Conferencing policy</p></td>
<td><p><strong>Get-CsConferencingPolicy</strong></p></td>
</tr>
<tr class="odd">
<td><p>Dial-in access numbers</p></td>
<td><p><strong>Get-CsDialInConferencingAccessNumber</strong></p></td>
</tr>
<tr class="even">
<td><p>Dial plans</p></td>
<td><p><strong>Get-CsDialPlan</strong></p></td>
</tr>
<tr class="odd">
<td><p>Voice policy</p></td>
<td><p><strong>Get-CsVoicePolicy</strong></p></td>
</tr>
<tr class="even">
<td><p>Voice routes</p></td>
<td><p><strong>Get-CsVoiceRoute</strong></p></td>
</tr>
<tr class="odd">
<td><p>PSTN Usage</p></td>
<td><p><strong>Get-CsPstnUsage</strong></p></td>
</tr>
<tr class="even">
<td><p>URLs</p></td>
<td><p><strong>Get-CsSimpleUrlConfiguration</strong></p></td>
</tr>
<tr class="odd">
<td><p>External access policies</p></td>
<td><p><strong>Get-CsExternalAccessPolicy</strong></p></td>
</tr>
<tr class="even">
<td><p>Archiving policy</p></td>
<td><p><strong>Get-CsArchivingPolicy</strong></p></td>
</tr>
</tbody>
</table>

