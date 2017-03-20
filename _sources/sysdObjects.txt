SYSD Model Objects
============================================

*config/SystemParam*
------------------------------------

- **Vrf**
	- **Data Type**: string
	- **Description**: System Vrf.
	- This parameter is key element.
	- **Default**: default
- **Hostname**
	- **Data Type**: string
	- **Description**: System Host Name.
- **MgmtIp**
	- **Data Type**: string
	- **Description**: Management Ip of System.
- **SwVersion**
	- **Data Type**: string
	- **Description**: FlexSwitch Version Information.
- **SwitchMac**
	- **Data Type**: string
	- **Description**: Switch Mac Address.
- **Description**
	- **Data Type**: string
	- **Description**: System Description.


*config/SystemLogging*
------------------------------------

- **Vrf**
	- **Data Type**: string
	- **Description**: Vrf name.
	- This parameter is key element.
	- **Default**: default
- **Logging**
	- **Data Type**: string
	- **Description**: Global logging.
	- **Default**: on


*state/SystemParam*
------------------------------------

- **Vrf**
	- **Data Type**: string
	- **Description**: System Vrf.
	- This parameter is key element.
- **Description**
	- **Data Type**: string
	- **Description**: System Description.
- **Distro**
	- **Data Type**: string
	- **Description**: Linux distro running on this system.
- **Hostname**
	- **Data Type**: string
	- **Description**: System Host Name.
- **Kernel**
	- **Data Type**: string
	- **Description**: Kernel version running on this system.
- **MgmtIp**
	- **Data Type**: string
	- **Description**: Management Ip of System.
- **SwVersion**
	- **Data Type**: string
	- **Description**: FlexSwitch Version Information.
- **SwitchMac**
	- **Data Type**: string
	- **Description**: Switch Mac Address.


*config/ComponentLogging*
------------------------------------

- **Module**
	- **Data Type**: string
	- **Description**: Module name to set logging level.
	- This parameter is key element.
- **Level**
	- **Data Type**: string
	- **Description**: Logging level.
	- **Default**: info


*state/Daemon*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Daemon name.
	- This parameter is key element.
- **RestartReason**
	- **Data Type**: string
	- **Description**: Last restart reason.
- **StartTime**
	- **Data Type**: string
	- **Description**: Daemon start time.
- **Enable**
	- **Data Type**: bool
	- **Description**: If the daemon configured to be enabled.
- **Reason**
	- **Data Type**: string
	- **Description**: Reason for current state of the daemon.
- **State**
	- **Data Type**: string
	- **Description**: State of the daemon.
- **KeepAlive**
	- **Data Type**: string
	- **Description**: KeepAlive state of the daemon.
- **RestartCount**
	- **Data Type**: int32
	- **Description**: Number of times this daemon has been restarted.
- **RestartTime**
	- **Data Type**: string
	- **Description**: Last restart time.


