﻿---
title: Configure XMPP gateway access policies and certificates
TOCTitle: Configure XMPP gateway access policies and certificates
ms:assetid: fac02f4e-d14d-4be3-b53c-74c82436fd93
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721945(v=OCS.15)
ms:contentKeyID: 49733882
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Configure XMPP gateway access policies and certificates

 


XMPP federation defines an external deployment based on the eXtensible Messaging and Presence Protocol (XMPP). An XMPP configuration allows Lync users access to XMPP domain users by:

  - IM and Presence – person to person only

  - Creation of XMPP federated contacts in the Lync client

When you configure policies for support of extensible messaging and presence protocol (XMPP) federated partners, the policies apply to users of XMPP federated domains, but not to users of session initiation protocol (SIP) instant messaging (IM) service providers (for example, Windows Live), or SIP federated domains. You configure an XMPP Federated Partner for each XMPP federated domain that you want to allow your users to add contacts and communicate with. Once the policies are in place, you need to configure the XMPP Gateway certificates.


> [!NOTE]
> To begin the XMPP Gateway migration, you need to deploy the Lync Server 2013 XMPP Gateway, and configure access policies to enable users for Lync Server 2013 XMPP Gateway. All users must be moved to the Lync Server 2013 deployment before you perform these steps. For details, see <A href="configure-xmpp-gateway-on-lync-server-2013.md">Configure XMPP gateway on Lync Server 2013</A>.



## Configure an External Access Policy to Enable Users for Lync Server 2013 XMPP Gateway

1.  Open Lync Server Control Panel.

2.  In the left navigation bar, click **Federation and External Access**, and then click **External Access Policy**.

3.  Click **New** and then click **User policy**.

4.  Enter a name for the external access user policy.

5.  Provide a description for external access user policy.

6.  Select **Enable communications with federated users**.

7.  Select **Enable communications with XMPP federated users**.

8.  Click **Commit** to save your changes to the site or user policy.

