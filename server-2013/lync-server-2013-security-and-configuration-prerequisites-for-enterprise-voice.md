---
title: 'Lync Server 2013: Security and configuration prerequisites for Enterprise Voice'
TOCTitle: Security and configuration prerequisites for Enterprise Voice
ms:assetid: 15354abe-733e-466b-bcd4-a6cfbf58caf8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398221(v=OCS.15)
ms:contentKeyID: 48183495
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Security and configuration prerequisites for Enterprise Voice in Lync Server 2013

 


Verify that your infrastructure meets the following security, user configuration, and scenario-specific hardware prerequisites.

## Administrative Rights and Certificate Infrastructure

Be sure that your environment is configured with the following administrative user groups and certificate infrastructure for use during the Enterprise Voice deployment process.

  - Administrators deploying Enterprise Voice should be members of the RTCUniversalServerAdmins group.

  - Administrators performing the configuration tasks must have adequate rights:
    
      - **CsVoiceAdministrator:** This administrator role can perform voice configuration tasks, manage voice applications, and assign voice policies to end users.
    
      - **CsUserAdministrator:** This administrator role can manage user properties, such as enabling Enterprise Voice for a user. This administrator role can also assign per-user policies, with the exception of the archiving policy; move users; and manage common area phones and analog devices.
    
      - **CsAdministrator:** This administrator role can perform all of the tasks of CsVoiceAdministrator and CsUserAdministrator.
    

    > [!NOTE]
    > Delegation enables more administrators to participate in your Lync Server deployment without opening up unnecessary access to resources.



  - Managed key infrastructure (MKI) is deployed and configured, by using either a Microsoft or a third-party certification authority (CA) infrastructure.
    

    > [!NOTE]
    > For details about certificate requirements in Lync Server, see <A href="lync-server-2013-certificate-infrastructure-requirements.md">Certificate infrastructure requirements for Lync Server 2013</A> in the Planning documentation.



## User Configuration

If you collocated the Mediation Server with each Front End pool or Standard Edition server during Front End deployment, user settings necessary for Enterprise Voice were configured automatically during installation of the files for those server roles.

If you are newly deploying the Enterprise Voice workload at this time, before you begin the deployment process, designate a primary phone number for each user who you plan to enable for Enterprise Voice. As the administrator, you are responsible for ensuring that this number is unique. Before implementation, all primary phone numbers must be normalized (correctly formatted) and copied to each user’s **Line URI** property using Lync Server Control Panel.


> [!NOTE]
> For examples of primary phone numbers required for Enterprise Voice deployment, see the <A href="lync-server-2013-dial-plans-and-normalization-rules.md">Dial plans and normalization rules in Lync Server 2013</A> section of <A href="lync-server-2013-dial-plans-and-normalization-rules.md">Dial plans and normalization rules in Lync Server 2013</A> in the Planning documentation.



## Next Steps: Install Files or Configure PSTN Connectivity

After verifying software and environmental prerequisites for Enterprise Voice, you can use the following content to either:

  - Install the Mediation Server, as described in [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md), but only if you want to deploy a stand-alone Mediation Server or pool because Mediation Servers are installed as part of the Front End pool or Standard Edition server deployment process when collocated.

  - Or, begin configuring settings to route calls for Enterprise Voice users, as described in [Configuring trunks in Lync Server 2013](lync-server-2013-configuring-trunks.md).

