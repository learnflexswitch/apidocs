DWDMModule Object
=============================================================

*config/DWDMModule*
------------------------------------

- Multiple objects of this type can exist in a system.

+---------------------+---------------+--------------------------------+-------------+------------------+
| **PARAMETER NAME**  | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+---------------------+---------------+--------------------------------+-------------+------------------+
| ModuleId **[KEY]**  | uint8         | DWDM Module identifier         | N/A         | N/A              |
+---------------------+---------------+--------------------------------+-------------+------------------+
| IndependentLaneMode | bool          | Network lane configuration     | true        | N/A              |
|                     |               | for the DWDM Module.           |             |                  |
|                     |               | true-Independent lanes         |             |                  |
+---------------------+---------------+--------------------------------+-------------+------------------+
| PMInterval          | uint8         | Performance monitoring         |           1 | N/A              |
|                     |               | interval                       |             |                  |
+---------------------+---------------+--------------------------------+-------------+------------------+
| AdminState          | string        | Reset state of this dwdm       | DOWN        | UP, DOWN         |
|                     |               | module (false (Reset           |             |                  |
|                     |               | deasserted)                    |             |                  |
+---------------------+---------------+--------------------------------+-------------+------------------+
| EnableExtPMTickSrc  | bool          | Enable/Disable external        | false       | N/A              |
|                     |               | tick source for performance    |             |                  |
|                     |               | monitoring                     |             |                  |
+---------------------+---------------+--------------------------------+-------------+------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/config/DWDMModule
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/DWDMModule/<uuid>
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/config/DWDMModules?CurrentMarker=<x>&Count=<y>
	- UPDATE(PATCH) By Key
		 curl -X PATCH -H 'Content-Type: application/json' -d '{<Model Object as json data>}'  http://device-management-IP:8080/public/v1/config/DWDMModule
	- UPDATE(PATCH) By ID
		 curl -X PATCH -H 'Content-Type: application/json' -d '{<Model Object as json data>}'  http://device-management-IP:8080/public/v1/config/DWDMModule<uuid>


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
		response, error = swtch.getDWDMModule(ModuleId=moduleid)

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
		response, error = swtch.getDWDMModuleById(ObjectId=objectid)

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
		response, error = swtch.getAllDWDMModules()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'




- **UPDATE**

::

	import sys
	import os
	from flexswitchV2 import FlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = FlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.updateDWDMModule(ModuleId=moduleid, IndependentLaneMode=independentlanemode, PMInterval=pminterval, AdminState=adminstate, EnableExtPMTickSrc=enableextpmticksrc)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


- **UPDATE By ID**

::

	import sys
	import os
	from flexswitchV2 import FlexSwitch

	if __name__ == '__main__':
		switchIP := "192.168.56.101"
		swtch = FlexSwitch (switchIP, 8080)  # Instantiate object to talk to flexSwitch
		response, error = swtch.updateDWDMModuleById(ObjectId=objectidIndependentLaneMode=independentlanemode, PMInterval=pminterval, AdminState=adminstate, EnableExtPMTickSrc=enableextpmticksrc)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'
