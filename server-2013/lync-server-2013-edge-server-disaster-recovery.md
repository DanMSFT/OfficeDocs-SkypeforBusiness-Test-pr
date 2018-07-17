---
title: 'Lync Server 2013: Edge Server disaster recovery'
TOCTitle: Edge Server disaster recovery
ms:assetid: 05ec8d26-d167-4a6f-a966-a1f8873cf974
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687960(v=OCS.15)
ms:contentKeyID: 49733545
ms.date: 04/27/2018
mtps_version: v=OCS.15
---

# Edge Server disaster recovery in Lync Server 2013

 


As with other server roles, the best way for you to provide high availability for your Edge servers is to deploy multiple Edge servers in pools in each site. If one Edge server goes down, the other servers in the pool will continue to provide Edge services.

To enable disaster recovery procedures, you must have separate Edge server pools deployed at separate sites. You do not have to explicitly pair Edge pools together as you do for Front End pools. However, having multiple Edge pools provides the available resources to continue operating if one entire Edge pool goes down. The following sections provide details about disaster recovery for the various functions of Edge servers.

## Remote Access

If you have multiple sites, each with a pool of Edge servers, and one entire Edge pool fails, the remote access services continue to function without requiring administrator action. When you create Edge pools in different sites, you cannot use the same FQDN. Each Edge pool must have unique FQDNs (internal and external). The Edge pools do not use reverse proxy publishing rules to talk to the Front End servers. Automatic failover occurs when the client requeries the remote access DNS service records, and remote users are routed to the Edge servers in another site. The client tries each external Edge FQDN according to the priority of the DNS SRV records.


> [!NOTE]
> For failover to work smoothly, ensure that the firewall allows the Front End servers from every pool to communicate with all Edge servers.



## Federation

For federation relationships with other organizations that are running Lync Server, inbound federation requests continue to work as long you have at least one access Edge server that is published and that uses DNS LB across multiple IP addresses. Any federation requests that come to an Edge pool IP that is down will fail back and then connect to an Edge pool IP that is running.

Outbound federation is always set up through one published Edge pool or Edge server in the organization. If this Edge pool has gone down, you must use Topology Builder to change the outbound federation route to use an Edge pool that is still running. For details, see [Failing over the Edge pool used for Lync Server federation in Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md).

## XMPP Federation

For XMPP federation, both outbound and inbound traffic will fail if the Edge pool that is designated as the XMPP federation gateway goes down. To make XMPP federation work again, you must change XMPP federation to use a different Edge pool. For details, see [Failing over the Edge pool used for XMPP federation in Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md).

## Edge Pool Fails But Front End Pool Is Still Running

If an Edge pool fails at a site, but the Front End pool at that site is still running, you must change the Front End pool to use a different Edge pool at a different site while that first Edge pool is down. For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).

