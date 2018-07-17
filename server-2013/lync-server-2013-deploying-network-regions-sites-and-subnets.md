---
title: 'Lync Server 2013: Deploying network regions, sites, and subnets'
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
mtps_version: v=OCS.15
---

# Deploying network regions, sites, and subnets in Lync Server 2013

 


Once Enterprise Voice is deployed, you need to configure:

  - Network regions

  - Network sites

  - Network subnets

## Define Network Regions

Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

For more information, see [New-CsNetworkRegion](https://technet.microsoft.com/en-us/library/gg425829\(v=ocs.15\)).

For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"


## Define Network Sites

Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

For more information, see [New-CsNetworkSite](https://technet.microsoft.com/en-us/library/gg398365\(v=ocs.15\)).

For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario. Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Site 1 (Delhi)</th>
<th>Site 2 (Hyderabad)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Site ID</p></td>
<td><p>Site 1 (Delhi)</p></td>
<td><p>Site 2 (Hyderabad)</p></td>
</tr>
<tr class="even">
<td><p>Region ID</p></td>
<td><p>Region 1 (India)</p></td>
<td><p>Region 1 (India)</p></td>
</tr>
</tbody>
</table>



## Define Network Subnets

Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

For more information, see [New-CsNetworkSubnet](https://technet.microsoft.com/en-us/library/gg398226\(v=ocs.15\)).

For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario. Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Site 1 (Delhi)</th>
<th>Site 2 (Hyderabad)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Subnet ID</p></td>
<td><p>192.168.0.0</p></td>
<td><p>192.168.1.0</p></td>
</tr>
<tr class="even">
<td><p>Mask</p></td>
<td><p>24</p></td>
<td><p>24</p></td>
</tr>
<tr class="odd">
<td><p>Site ID</p></td>
<td><p>Site 1 (Delhi)</p></td>
<td><p>Site 2 (Hyderabad)</p></td>
</tr>
</tbody>
</table>



## See Also


[Configuring Location-Based Routing in Lync Server 2013](lync-server-2013-configuring-location-based-routing.md)

