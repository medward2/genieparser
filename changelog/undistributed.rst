* Please follow the template we introduced in NOVEMBER.md file.
* Every parser need to be added under the corresponding feature.

| Module                  | Version       |
| ------------------------|:-------------:|
| ``genie.libs.parser``   |               |

--------------------------------------------------------------------------------
                                New
--------------------------------------------------------------------------------

* JUNOS
    * ShowRouteTable
        * Added aditional testcase
    * Added ShowRouteAdvertisingProtocolDetail
        * show route advertising-protocol {protocol} {ip_address} {route} detail
    * Added ShowLldp
        * show lldp
    * Added ShowSystemStatistics for:
        * show system statistics
    * Added ShowSystemStatisticsNoForwarding or:
        * show system statistics no-forwarding
    * Updated ShowOspfDatabaseLsaidDetail:
        * added testcase
        *extended from ShowOspfDatabaseAdvertisingRouterSelfDetail


--------------------------------------------------------------------------------
                                Fix
--------------------------------------------------------------------------------

* IOSXE
    * Updated ShowIsisDatabaseDetail for code issue:
        * show isis database detail
    * Updated ShowBgpDetailSuperParser for code issue:
        * 'show bgp all detail'
        * 'show ip bgp all detail'
        * 'show bgp {address_family} vrf {vrf} detail'
        * 'show bgp {address_family} rd {rd} detail'
        * 'show ip bgp {address_family} vrf {vrf} detail'
        * 'show ip bgp {address_family} rd {rd} detail'
    * Updated ShowBootvar:
        * Modified the regex patterns to support various outputs.
* NXOS
    * Updated ShowMacAddressTableBase:
        * Modified the regex patterns to support various outputs.
    * Updated ShowIpArpDetailVrfAll:
        * Modified the regex patterns to support various outputs.
    * Update ShowIpRoute:
        * Modified the regex patterns to support various outputs.
    * Update ShowIpMrouteVrfAll:
        * Modified the regex patterns to support various outputs.
    * Update ShowIpv6MrouteVrfAll:
        * Modified the regex patterns to support various outputs.
    * Updated ShowRunningConfigInterface:
        * Added regex to support vpc
        * Added regex to support native vlan
        * Added regex to support switchport_mode access
        * Fixed regex to allow white spaces in description
* IOSXR
    * Update ShowIpv4VrfAllInterface
        * Update regex to support ':' character in VRF Name.
    * Updated ShowVrfAllDetail:
        * Modified the regex patterns to support various outputs.
    * Updated ShowControllersOptics:
        * Added more regex patterns to support various outputs.
    * Updated ShowIsisSchema:
        * Made the key 'protocols_redistributed' optional.
* JUNOS
    * Updated ShowRoute
        * Modified cli method to accept only ip_address as input
    * Updated ShowRouteTable
        * Modified cli method to take an additional parameter
    * Updated ShowRouteAdvertisingProtocol
        * Added {route} parameter option
    * Added MonitorInterfaceTraffic for:
        * monitor interface traffic
    * Updated ShowOspfOverview
        * Optional key issue resolved
    * Updated ShowInterfaceExtensive
        * No longer breaks on use and previously unused data is now used
    * Updated ShowOspfDatabaseExtensiveSchema
        * Optional key issue resolved
    * Updated ShowOspf3DatabaseExtensiveSchema
        * Optional key issue resolved
* IOSXE
    * Updated ShowIpInterface
        * Modified regex to accommodate different outputs