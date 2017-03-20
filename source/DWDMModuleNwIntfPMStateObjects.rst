DWDMModuleNwIntfPMState Object
=============================================================

*state/DWDMModuleNwIntfPM*
------------------------------------

- Multiple objects of this type can exist in a system.

+--------------------+------------------+--------------------------------+-------------+---------------------------+
| **PARAMETER NAME** |  **DATA TYPE**   |        **DESCRIPTION**         | **DEFAULT** |     **VALID VALUES**      |
+--------------------+------------------+--------------------------------+-------------+---------------------------+
| Class **[KEY]**    | string           | Class of PM Data               | CLASS-A     | CLASS-A, CLASS-B, CLASS-B |
+--------------------+------------------+--------------------------------+-------------+---------------------------+
| ModuleId **[KEY]** | uint8            | DWDM Module identifier         | N/A         | N/A                       |
+--------------------+------------------+--------------------------------+-------------+---------------------------+
| NwIntfId **[KEY]** | uint8            | DWDM Module network interface  | N/A         | N/A                       |
|                    |                  | identifier                     |             |                           |
+--------------------+------------------+--------------------------------+-------------+---------------------------+
| Resource **[KEY]** | string           | Opticd resource name for which | N/A         | N/A                       |
|                    |                  | PM Data is required            |             |                           |
+--------------------+------------------+--------------------------------+-------------+---------------------------+
| Type **[KEY]**     | string           | Min/Max/Avg                    | N/A         | N/A                       |
+--------------------+------------------+--------------------------------+-------------+---------------------------+
| Data               | DWDMModulePMData |                                | N/A         | N/A                       |
+--------------------+------------------+--------------------------------+-------------+---------------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/DWDMModuleNwIntfPM
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/DWDMModuleNwIntfPMs?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/DWDMModuleNwIntfPMState/<uuid>


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
		response, error = swtch.getDWDMModuleNwIntfPMState(Class=class, ModuleId=moduleid, NwIntfId=nwintfid, Resource=resource, Type=type)

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
		response, error = swtch.getDWDMModuleNwIntfPMStateById(ObjectId=objectid)

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
		response, error = swtch.getAllDWDMModuleNwIntfPMStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


