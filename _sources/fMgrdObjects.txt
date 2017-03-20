FMGRD Model Objects
============================================

*state/Alarm*
------------------------------------

- **OwnerName**
	- **Data Type**: string
	- **Description**: Alarm owner daemon name picked up from events.json.
	- This parameter is key element.
- **SrcObjName**
	- **Data Type**: string
	- **Description**: Alarm event name picked up from events.json.
	- This parameter is key element.
- **EventId**
	- **Data Type**: int32
	- **Description**: Alarm event id picked up from events.json.
	- This parameter is key element.
- **OwnerId**
	- **Data Type**: int32
	- **Description**: Alarm owner daemon Id picked up from events.json.
	- This parameter is key element.
- **EventName**
	- **Data Type**: string
	- **Description**: Alarm event name picked up from events.json.
	- This parameter is key element.
- **ResolutionReason**
	- **Data Type**: string
	- **Description**: Cleared/Disabled.
- **ResolutionTime**
	- **Data Type**: string
	- **Description**: Resolution Time stamp.
- **Severity**
	- **Data Type**: string
	- **Description**: Alarm Severity.
- **Description**
	- **Data Type**: string
	- **Description**: Description explaining the fault.
- **SrcObjUUID**
	- **Data Type**: string
	- **Description**: Fault Object UUID.
- **OccuranceTime**
	- **Data Type**: string
	- **Description**: Timestamp at which fault occured.
- **SrcObjKey**
	- **Data Type**: string
	- **Description**: Fault Object Key.


*config/FMgrGlobal*
------------------------------------

- **Vrf**
	- **Data Type**: string
	- **Description**: System Vrf.
	- This parameter is key element.
	- **Default**: default
- **Enable**
	- **Data Type**: bool
	- **Description**: Enable Fault Manager.


*state/Fault*
------------------------------------

- **EventId**
	- **Data Type**: int32
	- **Description**: Fault event id picked up from events.json.
	- This parameter is key element.
- **EventName**
	- **Data Type**: string
	- **Description**: Fault event name picked up from events.json.
	- This parameter is key element.
- **OwnerName**
	- **Data Type**: string
	- **Description**: Fault owner daemon name picked up from events.json.
	- This parameter is key element.
- **SrcObjName**
	- **Data Type**: string
	- **Description**: Fault event name picked up from events.json.
	- This parameter is key element.
- **OwnerId**
	- **Data Type**: int32
	- **Description**: Fault owner daemon Id picked up from events.json.
	- This parameter is key element.
- **ResolutionReason**
	- **Data Type**: string
	- **Description**: Cleared/Disabled.
- **ResolutionTime**
	- **Data Type**: string
	- **Description**: Resolution Time stamp.
- **Description**
	- **Data Type**: string
	- **Description**: Description explaining the fault.
- **OccuranceTime**
	- **Data Type**: string
	- **Description**: Timestamp at which fault occured.
- **SrcObjKey**
	- **Data Type**: string
	- **Description**: Fault Object Key.
- **SrcObjUUID**
	- **Data Type**: string
	- **Description**: Fault Object UUID.


