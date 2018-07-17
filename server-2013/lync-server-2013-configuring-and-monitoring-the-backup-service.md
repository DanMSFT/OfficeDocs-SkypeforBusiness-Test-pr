---
title: 'Lync Server 2013: Configuring and monitoring the Backup Service'
TOCTitle: Configuring and monitoring the Backup Service
ms:assetid: c608280e-a7d1-4ae0-a75c-da6b524752fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205252(v=OCS.15)
ms:contentKeyID: 48185365
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Configuring and monitoring the Backup Service in Lync Server 2013

 


You can use the following Lync Server Management Shell commands to configure and monitor the Backup Service.


> [!NOTE]
> The RTCUniversalServerAdmins group is the only group that has permissions to run <STRONG>Get-CsBackupServiceStatus</STRONG> by default. To use this cmdlet, log on as a member of this group. Or, you can grant access to this command to other groups (for example, CSAdministrator) by using the <STRONG>Set-CsBackupServiceConfiguration</STRONG> cmdlet.



## To see the Backup Service configuration

Run the following cmdlet:

    Get-CsBackupServiceConfiguration

The default for SyncInterval is two minutes.

## To set the Backup Service sync interval

Run the following cmdlet:

    Set-CsBackupServiceConfiguration -SyncInterval interval

For example, the following sets the interval to three minutes.

    Set-CsBackupServiceConfiguration -SyncInterval 00:03:00


> [!IMPORTANT]
> Although you can use this cmdlet to change the default sync interval for the Backup Service, you should not do so unless it is absolutely necessary, as the sync interval has a great impact on the Backup Service performance and the recovery point objective (RPO).



## To get the Backup Service status for a particular pool

Run the following cmdlet:

    Get-CsBackupServiceStatus -PoolFqdn <pool-FQDN>


> [!NOTE]
> The Backup Service sync status is defined unidirectionally from a pool (P1) to its backup pool (P2). The sync status from P1 to P2 can be different than the one from P2 to P1. For P1 to P2, Backup Service is in a “steady” state if all the changes made in P1 are completely replicated over to P2 within the sync interval. It is in the “final” state if there are no more changes to be synchronized from P1 to P2. Both states indicate a snapshot of the Backup Service at the time the cmdlet is executed. It does not imply that the state returned will stay as is afterwards. In particular, the “final” state will continue to hold only if P1 does not generate any changes after the cmdlet is executed. This is true in the case of failing P1 over to P2 after P1 is placed into the read-only mode as part of the <STRONG>Invoke-CsPoolfailover</STRONG> execution logic.



## To get information about the backup relationship for a particular pool

Run the following cmdlet:

    Get-CsPoolBackupRelationship -PoolFQDN <poolFQDN>

## To force a Backup Service sync

Run the following cmdlet:

    Invoke-CsBackupServiceSync -PoolFqdn <poolFqdn> [-BackupModule  {All|PresenceFocus|DataConf|CMSMaster}]

