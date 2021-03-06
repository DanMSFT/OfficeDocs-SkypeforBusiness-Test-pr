﻿---
title: 'Lync Server 2013: Planning for extensible messaging and presence protocol (XMPP) federation'
TOCTitle: Planning for extensible messaging and presence protocol (XMPP) federation
ms:assetid: 952b33e2-1f58-4831-9a39-1dfec2a316ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205107(v=OCS.15)
ms:contentKeyID: 48184892
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Planning for extensible messaging and presence protocol (XMPP) federation in Lync Server 2013

 


Previous versions of Lync Server and Office Communications Server provided an extensible messaging and presence protocol (XMPP) gateway that could be deployed as a separate server role to allow federating with XMPP deployments. In Microsoft Lync Server 2013, the XMPP functionality can be deployed as a feature. XMPP functionality is installed in two parts: an XMPP proxy that runs on the Edge Server and the XMPP gateway that runs on the Front End Servers.

Deployment and configuration of XMPP is covered in [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) You plan for supporting XMPP in your organization by defining port and protocol rules on your firewall, configuration of certificates, and adding DNS records. The following topics in this section summarize the information that you will need to successfully plan XMPP federation for your deployment.


> [!IMPORTANT]
> The XMPP capability of Lync Server 2013 is tested and supported by Microsoft for instant messaging federation with Google Talk. For any other XMPP systems contact the third-party vendor to verify that they support federation with Lync Server 2013, and for any deployment or troubleshooting recommendations.



## In This Section

  - [Certificate summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013](lync-server-2013-certificate-summary-extensible-messaging-and-presence-protocol-xmpp-federation.md)

  - [Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013](lync-server-2013-port-summary-extensible-messaging-and-presence-protocol-xmpp-federation.md)

  - [DNS summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013](lync-server-2013-dns-summary-extensible-messaging-and-presence-protocol-xmpp-federation.md)

## See Also


[Setting up XMPP federation in Lync Server 2013](lync-server-2013-setting-up-xmpp-federation.md)  
[Configure policies to control XMPP federated user access in Lync Server 2013](lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md)  


[Manage XMPP federated partners in Lync Server 2013](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
[Get-CsExternalAccessPolicy](https://technet.microsoft.com/en-us/library/gg425805\(v=ocs.15\))  
[Get-CsXmppAllowedPartner](https://technet.microsoft.com/en-us/library/jj204981\(v=ocs.15\))  
[Get-CsXmppGatewayConfiguration](https://technet.microsoft.com/en-us/library/jj204869\(v=ocs.15\))

