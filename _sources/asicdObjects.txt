ASICD Model Objects
============================================

*state/AsicGlobal*
------------------------------------

- **ModuleId**
	- **Data Type**: uint8
	- **Description**: Module identifier.
	- This parameter is key element.
- **VendorId**
	- **Data Type**: string
	- **Description**: Vendor identification value.
- **ModuleTemp**
	- **Data Type**: float64
	- **Description**: Current module temperature.
- **PartNumber**
	- **Data Type**: string
	- **Description**: Part number of underlying switching asic.
- **RevisionId**
	- **Data Type**: string
	- **Description**: Revision ID of underlying switching asic.


*config/EthernetPM*
------------------------------------

- **Resource**
	- **Data Type**: string
	- **Description**: Resource identifier.
	- This parameter is key element.
	- **Possible Values**: StatUnderSizePkts, StatOverSizePkts, StatFragments, StatCRCAlignErrors, StatJabber, StatEtherPkts, StatMCPkts, StatBCPkts, Stat64OctOrLess, Stat65OctTo126Oct, Stat128OctTo255Oct, Stat128OctTo255Oct, Stat256OctTo511Oct, Stat512OctTo1023Oct, Statc1024OctTo1518Oct
- **IntfRef**
	- **Data Type**: string
	- **Description**: Interface name of port.
	- This parameter is key element.
- **LowAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Low alarm threshold value for this PM.
	- **Default**: -100000
- **PMClassAEnable**
	- **Data Type**: bool
	- **Description**: Enable/Disable control for CLASS-A PM.
	- **Default**: true
- **PMClassCEnable**
	- **Data Type**: bool
	- **Description**: Enable/Disable control for CLASS-C PM.
	- **Default**: true
- **LowWarnThreshold**
	- **Data Type**: float64
	- **Description**: Low warning threshold value for this PM.
	- **Default**: -100000
- **PMClassBEnable**
	- **Data Type**: bool
	- **Description**: Enable/Disable control for CLASS-B PM.
	- **Default**: true
- **HighAlarmThreshold**
	- **Data Type**: float64
	- **Description**: High alarm threshold value for this PM.
	- **Default**: 100000
- **HighWarnThreshold**
	- **Data Type**: float64
	- **Description**: High warning threshold value for this PM.
	- **Default**: 100000


*state/Vlan*
------------------------------------

- **VlanId**
	- **Data Type**: int32
	- **Description**: 802.1Q tag/Vlan ID for vlan being provisioned.
	- This parameter is key element.
- **IfIndex**
	- **Data Type**: int32
	- **Description**: System assigned interface id for this vlan interface.
- **OperState**
	- **Data Type**: string
	- **Description**: Operational state of vlan interface.
- **VlanName**
	- **Data Type**: string
	- **Description**: System assigned vlan name.


*state/AsicGlobalPM*
------------------------------------

- **ModuleId**
	- **Data Type**: uint8
	- **Description**: Module identifier.
	- This parameter is key element.
- **Resource**
	- **Data Type**: string
	- **Description**: Resource identifier.
	- This parameter is key element.
- **ClassBPMData**
	- **Data Type**: PMData
	- **Description**: PM Data corresponding to PM Class B.
- **ClassCPMData**
	- **Data Type**: PMData
	- **Description**: PM Data corresponding to PM Class C.
- **ClassAPMData**
	- **Data Type**: PMData
	- **Description**: PM Data corresponding to PM Class A.


*config/Port*
------------------------------------

- **IntfRef**
	- **Data Type**: string
	- **Description**: Front panel port name or system assigned interface id.
	- This parameter is key element.
- **AdminState**
	- **Data Type**: string
	- **Description**: Administrative state of this port.
	- **Default**: DOWN
- **BreakOutMode**
	- **Data Type**: string
	- **Description**: Break out mode for the port. Only applicable on ports that support breakout. Valid modes - 1x40.
- **Duplex**
	- **Data Type**: string
	- **Description**: Duplex setting for this port.
	- **Default**: Full Duplex
- **MediaType**
	- **Data Type**: string
	- **Description**: Type of media inserted into this port.
- **Mtu**
	- **Data Type**: int32
	- **Description**: Maximum transmission unit size for this port.
- **Autoneg**
	- **Data Type**: string
	- **Description**: Autonegotiation setting for this port.
	- **Default**: OFF
- **Description**
	- **Data Type**: string
	- **Description**: User provided string description.
	- **Default**: FP Port
- **IfIndex**
	- **Data Type**: int32
	- **Description**: System assigned interface id for this port. Read only attribute.
- **LoopbackMode**
	- **Data Type**: string
	- **Description**: Desired loopback setting for this port.
	- **Default**: NONE
- **EnableFEC**
	- **Data Type**: bool
	- **Description**: Enable/Disable 802.3bj FEC on this interface.
	- **Default**: false
- **MacAddr**
	- **Data Type**: string
	- **Description**: Mac address associated with this port.
- **PhyIntfType**
	- **Data Type**: string
	- **Description**: Type of internal phy interface.
- **Speed**
	- **Data Type**: int32
	- **Description**: Port speed in Mbps.


*state/EthernetPM*
------------------------------------

- **Resource**
	- **Data Type**: string
	- **Description**: Resource identifier.
	- This parameter is key element.
- **IntfRef**
	- **Data Type**: string
	- **Description**: Interface name of port.
	- This parameter is key element.
- **ClassAPMData**
	- **Data Type**: PMData
	- **Description**: PM Data corresponding to PM Class A.
- **ClassBPMData**
	- **Data Type**: PMData
	- **Description**: PM Data corresponding to PM Class B.
- **ClassCPMData**
	- **Data Type**: PMData
	- **Description**: PM Data corresponding to PM Class C.


*config/Vlan*
------------------------------------

- **VlanId**
	- **Data Type**: int32
	- **Description**: 802.1Q tag/Vlan ID for vlan being provisioned.
	- This parameter is key element.
- **IntfList**
	- **Data Type**: string
	- **Description**: List of interface names or ifindex values to  be added as tagged members of the vlan.
- **UntagIntfList**
	- **Data Type**: string
	- **Description**: List of interface names or ifindex values to  be added as untagged members of the vlan.


*config/AsicGlobalPM*
------------------------------------

- **Resource**
	- **Data Type**: string
	- **Description**: Resource identifier.
	- This parameter is key element.
	- **Possible Values**: Temperature
- **ModuleId**
	- **Data Type**: uint8
	- **Description**: Module identifier.
	- This parameter is key element.
- **HighAlarmThreshold**
	- **Data Type**: float64
	- **Description**: High alarm threshold value for this PM.
	- **Default**: 100000
- **HighWarnThreshold**
	- **Data Type**: float64
	- **Description**: High warning threshold value for this PM.
	- **Default**: 100000
- **LowAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Low alarm threshold value for this PM.
	- **Default**: -100000
- **LowWarnThreshold**
	- **Data Type**: float64
	- **Description**: Low warning threshold value for this PM.
	- **Default**: -100000
- **PMClassCEnable**
	- **Data Type**: bool
	- **Description**: Enable/Disable control for CLASS-C PM.
	- **Default**: true
- **PMClassAEnable**
	- **Data Type**: bool
	- **Description**: Enable/Disable control for CLASS-A PM.
	- **Default**: true
- **PMClassBEnable**
	- **Data Type**: bool
	- **Description**: Enable/Disable control for CLASS-B PM.
	- **Default**: true


*state/Port*
------------------------------------

- **IntfRef**
	- **Data Type**: string
	- **Description**: Front panel port name or system assigned interface id.
	- This parameter is key element.
- **IfIndex**
	- **Data Type**: int32
	- **Description**: System assigned interface id for this port.
- **LastDownEventTime**
	- **Data Type**: string
	- **Description**: Timestamp corresponding to the last UP to DOWN operational state change event.
- **ConfigMode**
	- **Data Type**: string
	- **Description**: The current mode of configuration on this port (L2/L3/Internal).
- **IfEtherPkts128To255Octets**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet packets sized between 128 and 255 bytes.
- **IfInDiscards**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of inbound packets that were discarded.
- **IfOutDiscards**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of error free packets discarded and not transmitted.
- **IfEtherFragments**
	- **Data Type**: int64
	- **Description**: RFC1757 Total number of ethernet fragments received and transmitted.
- **IfEtherPkts**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet packets received and transmitted.
- **IfEtherPkts1024To1518Octets**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet packets sized between 1024 and 1518 bytes.
- **LastUpEventTime**
	- **Data Type**: string
	- **Description**: Timestamp corresponding to the last DOWN to UP operational state change event.
- **PresentInHW**
	- **Data Type**: string
	- **Description**: Indication of whether this port object maps to a physical port. Set to 'No' for ports that are not broken out..
- **IfEtherBcastPkts**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet broadcast packets received and transmitted.
- **IfEtherCRCAlignError**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of CRC alignment errors.
- **IfEtherUnderSizePktCnt**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total numbe of undersized packets received and transmitted.
- **IfEtherPkts65To127Octets**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet packets sized between 65 and 127 bytes.
- **IfOutUcastPkts**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of unicast packets transmitted on this port.
- **IfOutOctets**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of octets transmitted on this port.
- **NumUpEvents**
	- **Data Type**: int32
	- **Description**: Number of times the operational state transitioned from DOWN to UP.
- **IfEtherMCPkts**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of multicast packets received and transmitted.
- **IfInUcastPkts**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of unicast packets received on this port.
- **IfInUnknownProtos**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of inbound packets discarded due to unknown protocol.
- **OperState**
	- **Data Type**: string
	- **Description**: Operational state of front panel port.
- **IfEtherPkts256To511Octets**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet packets sized between 256 and 511 bytes.
- **IfInErrors**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of inbound packets that contained an error.
- **IfOutErrors**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of packets discarded and not transmitted due to packet errors.
- **IfEtherJabber**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of jabber frames received and transmitted.
- **NumDownEvents**
	- **Data Type**: int32
	- **Description**: Number of times the operational state transitioned from UP to DOWN.
- **IfEtherPkts64OrLessOctets**
	- **Data Type**: int64
	- **Description**: RFC1757 Total number of ethernet packets sized 64 bytes or lesser.
- **IfInOctets**
	- **Data Type**: int64
	- **Description**: RFC2233 Total number of octets received on this port.
- **Name**
	- **Data Type**: string
	- **Description**: System assigned vlan name.
- **Pvid**
	- **Data Type**: int32
	- **Description**: The vlanid assigned to untagged traffic ingressing this port.
- **ErrDisableReason**
	- **Data Type**: string
	- **Description**: Reason explaining why port has been disabled by protocol code.
- **IfEtherOverSizePktCnt**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of oversized packets received and transmitted.
- **IfEtherPkts512To1023Octets**
	- **Data Type**: int64
	- **Description**: RFC 1757 Total number of ethernet packets sized between 512 and 1023 bytes.


*state/MacTableEntry*
------------------------------------

- **MacAddr**
	- **Data Type**: string
	- **Description**: MAC Address.
	- This parameter is key element.
- **Port**
	- **Data Type**: int32
	- **Description**: Port number on which mac was learned.
	- **Default**: 0
- **VlanId**
	- **Data Type**: int32
	- **Description**: Vlan id corresponding to which mac was learned.
	- **Default**: 0


