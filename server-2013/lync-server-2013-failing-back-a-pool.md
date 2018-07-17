---
title: 'Lync Server 2013: Failing back a pool'
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Failing back a pool in Lync Server 2013

 


After the pool that experienced the disaster is back online (that is, Pool1 in this example), take the following steps to restore your deployment to regular working status.

Note that the failback process takes several minute to complete.  For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.

1.  Fail back the users who were originally homed in Pool1 and have been failed over to Pool2 by typing the following cmdlet:
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

No other steps are necessary. If you failed over the Central Management Server, you can leave it in Pool2.

