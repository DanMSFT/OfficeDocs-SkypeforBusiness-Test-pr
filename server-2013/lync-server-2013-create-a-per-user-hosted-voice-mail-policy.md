---
title: 'Lync Server 2013: Create a per-user hosted voice mail policy'
TOCTitle: Create a per-user hosted voice mail policy
ms:assetid: 39018a7c-e0c3-46a2-be4e-05604ec67a50
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425867(v=OCS.15)
ms:contentKeyID: 48183902
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Create a per-user hosted voice mail policy in Lync Server 2013

 


A *per-user* policy can only impact individual users, groups, and contact objects. To deploy a per-user policy, you must explicitly assign the policy to one or more users, groups, or contact objects. For details, see [Assign a per-user hosted voice mail policy in Lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md).

For details about working with per-user hosted voice mail policies, see the Lync Server Management Shell documentation for the following cmdlets:

  - [New-CsHostedVoicemailPolicy](https://technet.microsoft.com/en-us/library/gg398653\(v=ocs.15\))

  - [Set-CsHostedVoicemailPolicy](https://technet.microsoft.com/en-us/library/gg412722\(v=ocs.15\))

  - [Get-CsHostedVoicemailPolicy](https://technet.microsoft.com/en-us/library/gg398348\(v=ocs.15\))

## To create a per-user hosted voice mail policy

1.  Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.

2.  Run the New-CsHostedVoicemailPolicy cmdlet to create the policy. For example, run:
    
        New-CsHostedVoicemailPolicy -Identity ExRedmond -Destination ExUM.fabrikam.com -Description "Hosted voice mail policy for Redmond users." -Organization "corp1.litwareinc.com, corp2.litwareinc.com"
    
    The previous example creates a hosted voice mail policy with per-user scope, and sets the following parameters:
    
      - **Identity** specifies a unique identifier for the policy, which includes the scope. For a policy with per-user scope, this parameter value is specified as a simple string, for example, ExRedmond.
    
      - **Destination** specifies the fully qualified domain name (FQDN) of the hosted Exchange UM service. This parameter is optional, but if you attempt to enable a user for hosted voice mail and the user’s assigned policy does not have a Destination value, the enable will fail.
    
      - **Description** provides optional descriptive information about the policy.
    
      - **Organization** specifies a comma-separated list of the Exchange tenants that home Lync Server 2013 users. Each tenant must be specified as the FQDN of that tenant on the hosted Exchange UM service.

## See Also


[Assign a per-user hosted voice mail policy in Lync Server 2013](lync-server-2013-assign-a-per-user-hosted-voice-mail-policy.md)

