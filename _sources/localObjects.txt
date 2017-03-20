LOCAL Model Objects
============================================

*state/SystemSwVersion*
------------------------------------

- **FlexswitchVersion**
	- **Data Type**: string
	- **Description**: Flexswitch version.
	- This parameter is key element.
- **Repos**
	- **Data Type**: RepoInfo
	- **Description**: Git repo details.


*state/XponderGlobal*
------------------------------------

- **XponderId**
	- **Data Type**: uint8
	- **Description**: Xponder module identifier.
	- This parameter is key element.
- **XponderDescription**
	- **Data Type**: string
	- **Description**: User configurable description string for the xponder module.
- **XponderMode**
	- **Data Type**: string
	- **Description**: Global operational mode of Xponder module.


*state/ConfigLog*
------------------------------------

- **Time**
	- **Data Type**: string
	- **Description**: When the API was called.
	- This parameter is key element.
- **API**
	- **Data Type**: string
	- **Description**: Name of the API called.
	- This parameter is key element.
- **SeqNum**
	- **Data Type**: uint32
	- **Description**: Sequence number of the API call.
	- This parameter is key element.
- **UserAddr**
	- **Data Type**: string
	- **Description**: Host address from where the call was made.
- **UserName**
	- **Data Type**: string
	- **Description**: User who made the call.
- **Data**
	- **Data Type**: string
	- **Description**: User provided data.
- **Operation**
	- **Data Type**: string
	- **Description**: Oprtation executed on this API.
- **Result**
	- **Data Type**: string
	- **Description**: Result of the API call.


*state/ApiInfo*
------------------------------------

- **Url**
	- **Data Type**: string
	- **Description**: URL.
	- This parameter is key element.
- **Info**
	- **Data Type**: string
	- **Description**: APIs available under this URL or details of the specific API.


*config/XponderGlobal*
------------------------------------

- **XponderId**
	- **Data Type**: uint8
	- **Description**: Xponder module identifier.
	- This parameter is key element.
	- **Default**: 0
- **XponderDescription**
	- **Data Type**: string
	- **Description**: User configurable description string for the xponder module.
	- **Default**: This is a Voyager platform
- **XponderMode**
	- **Data Type**: string
	- **Description**: Global operational mode of Xponder module.
	- **Default**: OutOfService


*state/SystemStatus*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Name of the system.
	- This parameter is key element.
- **UpTime**
	- **Data Type**: string
	- **Description**: Uptime of this system.
- **NumGetCalls**
	- **Data Type**: string
	- **Description**: Number of get api calls made.
- **NumCreateCalls**
	- **Data Type**: string
	- **Description**: Number of create api calls made.
- **NumDeleteCalls**
	- **Data Type**: string
	- **Description**: Number of delete api calls made.
- **NumUpdateCalls**
	- **Data Type**: string
	- **Description**: Number of update api calls made.
- **Ready**
	- **Data Type**: bool
	- **Description**: System is ready to accept api calls.
- **Reason**
	- **Data Type**: string
	- **Description**: Reason if system not ready.
- **FlexDaemons**
	- **Data Type**: DaemonState
	- **Description**: Daemon states.
- **NumActionCalls**
	- **Data Type**: string
	- **Description**: Number of action api calls made.


