---
title: 'Lync Server 2013: Overview of the Lync Server hybrid environment'
TOCTitle: Overview of the Lync Server 2013 hybrid environment
ms:assetid: 0d16ec3a-28f0-4483-96e7-8e68f30398fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204669(v=OCS.15)
ms:contentKeyID: 48183399
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Overview of the Lync Server 2013 hybrid environment

 


Lync Server 2013 hybrid environment refers to a deployment in which there are some users homed to the on-premises Lync Server 2013 and other users homed to Lync Online, but users share the same domain, such as user@contoso.com.

## About this Guide

This guide describes the tasks necessary to configure your Lync Server 2013 environment for interoperability with Lync Online, and then to move users from your on-premises deployment to use Lync Online.

## Prerequisites

You will need to have the following applications and utilities installed to complete the tasks for configuring a deployment for hybrid. The installers for these files are included on the installation media provided for your deployment, as well as at the links included in the following list.

  - [Active Directory Federation Services (AD FS) 2.0](http://go.microsoft.com/fwlink/p/?linkid=257305)

  - [Microsoft Directory Synchronization Tool 9.1](http://go.microsoft.com/fwlink/p/?linkid=257307)

  - [Install Windows PowerShell for single sign-on with AD FS](http://go.microsoft.com/fwlink/p/?linkid=398710)

  - Microsoft Online Services Sign-in Assistant (msoidcli-7.0.msi) is included with the Desktop Setup for Office 365, which can be obtained from the Downloads page linked to from the Office 365 Admin portal.

## Administrator Credentials

When you are asked to provide your administrator credentials, use the username and password for the administrator account for your Office 365 tenant. You will also use these credentials when you configure Active Directory Federation Services (AD FS) 2.0, Directory Synchronization, Single sign-on, federation, and moving users to Lync Online.

## Connecting to Lync Online PowerShell

Administrators now have the ability to use Windows PowerShell to manage Lync Online and their Lync Online user accounts. To do this, you must first download and install the Lync Online Connector Module from the Microsoft Download Center (http://go.microsoft.com/fwlink/?LinkId=294688). For more information on downloading, installing, and using the Lync Online Connector Module, and for detailed information on using Windows PowerShell to manage Lync Online, see [Using Windows PowerShell to manage Lync Online](https://technet.microsoft.com/en-us/library/dn362831\(v=ocs.15\)).

