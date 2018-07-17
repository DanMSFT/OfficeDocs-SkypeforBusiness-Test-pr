---
title: 'Lync Server 2013: Clients supported for Call Park'
TOCTitle: Clients supported for Call Park
ms:assetid: c236d2ba-9d83-418c-9cbc-92541f115fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412958(v=OCS.15)
ms:contentKeyID: 48185320
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Clients supported for Call Park in Lync Server 2013

 


This section identifies the clients that can be used to park calls and the clients that can be used to retrieve parked calls.

## Clients Supported for Parking Calls

Calls from any IP, private branch exchange (PBX), public switched telephone network (PSTN), or mobile phone can be parked.


> [!NOTE]
> Only audio calls can be parked. Instant messages and conferences cannot be parked.



The following clients can use Call Park to park calls:

  - Lync 2013

  - Lync 2010

  - Lync 2010 Attendant

  - Lync Phone Edition


> [!NOTE]
> Mobile phones cannot use Call Park to park calls.



## Clients Supported for Retrieving Calls

Orbit ranges are configured as blocks of virtual extensions (extensions without an assigned user or phone). When you configure orbits as virtual extensions, mobile phones and PSTN phones cannot retrieve parked calls.

Federated users cannot retrieve parked calls.

The following clients can retrieve calls that are parked on Call Park:

  - Lync 2013

  - Lync 2010

  - Lync 2010 Attendant

  - Lync Phone Edition

  - IP common area phones

  - Non-IP phones that are connected to the Lync Server 2013 infrastructure, including common area phones and private branch exchange (PBX) phones

