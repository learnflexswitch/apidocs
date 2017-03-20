DWDMModuleState Object
=============================================================

*state/DWDMModule*
------------------------------------

- Multiple objects of this type can exist in a system.

+------------------------+---------------+--------------------------------+-------------+------------------+
|   **PARAMETER NAME**   | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleId **[KEY]**     | uint8         | DWDM Module identifier         | N/A         | N/A              |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleActiveFWVersion  | string        | Firmware version of active     | N/A         | N/A              |
|                        |               | partition of dwdm module       |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleState            | string        | Current MSA state of dwdm      | N/A         | N/A              |
|                        |               | module                         |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| Populated              | bool          | Is module populated            | N/A         | N/A              |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleHWVersion        | string        | HW version of dwdm module      | N/A         | N/A              |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleStandByFWStatus  | string        | Firmware image status of       | N/A         | N/A              |
|                        |               | standby partition of dwdm      |             |                  |
|                        |               | module                         |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleTemp             | float64       | Module temperature in deg      | N/A         | N/A              |
|                        |               | Celsius                        |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| VendorSerialNum        | string        | Vendor assigned serial number  | N/A         | N/A              |
|                        |               | of dwdm module                 |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| VendorPartNum          | string        | Vendor assigned part number of | N/A         | N/A              |
|                        |               | dwdm module                    |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleStandByFWVersion | string        | Firmware version of standby    | N/A         | N/A              |
|                        |               | partition of dwdm module       |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleVoltage          | float64       | Module power supply voltage in | N/A         | N/A              |
|                        |               | Volts                          |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| VendorDateCode         | string        | Device manufacture data code   | N/A         | N/A              |
|                        |               | of dwdm module                 |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+
| VendorName             | string        | Vendor name of dwdm module     | N/A         | N/A              |
+------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleActiveFWStatus   | string        | Firmware image status of       | N/A         | N/A              |
|                        |               | active partition of dwdm       |             |                  |
|                        |               | module                         |             |                  |
+------------------------+---------------+--------------------------------+-------------+------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/DWDMModule
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/DWDMModules?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/DWDMModuleState/<uuid>


*FlexSwitch SDK API Supported:*
------------------------------------



- **GET**


::

	import sys
	import os
	from flexswitchV2 import FlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = FlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.getDWDMModuleState(ModuleId=moduleid)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


- **GET By ID**


::

	import sys
	import os
	from flexswitchV2 import FlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = FlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.getDWDMModuleStateById(ObjectId=objectid)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'




- **GET ALL**


::

	import sys
	import os
	from flexswitchV2 import FlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = FlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.getAllDWDMModuleStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


