---
title: Manage add-ins
TOCTitle: Manage add-ins
ms:assetid: b84f868e-b36e-4ab4-b284-7db212d401c3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205193(v=OCS.15)
ms:contentKeyID: 48185204
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Manage add-ins

 


To create a new Persistent Chat Server Add-in

    New-CsPersistentChatAddin -Name Contoso -PersistentChatPoolFqdn client.contoso.com -Url http://contoso.com 

## Create, Get, Set, or Remove an Add-in

To create a new Add-in

    New-CsPersistentChatAddin -PersistentChatPoolFqdn <String> -Name <String> -Url<String>


> [!IMPORTANT]
> PersistentChatPoolFqdn &lt;String&gt; is required only if there is more than one Persistent Chat Server pool.



To get an Add-in

    Get-CsPersistentChatAddin -Identity <String>]

or

    Get-CsPersistentChatAddin -PersistentChatPoolFqdn <String>

To set an Add-in

    Set-CsPersistentChatAddIn -Instance <AddinObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

or

    Set-CsPersistentChatAddIn -Identity <String> [-Name <String>] [-Url<String>] [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

To remove an Add-in

    Remove-CsPersistentChatAddIn -Instance <AddinObject> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

or

    Remove-CsPersistentChatAddIn -Identity <String> [-Force <Switch Parameter>] [-Confirm <Switch Parameter>]

