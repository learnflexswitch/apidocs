AsicGlobalPM Object
=============================================================

*config/AsicGlobalPM*
------------------------------------

- Only one object of this type can exist in a system.

+--------------------+---------------+--------------------------------+-------------+------------------+
| **PARAMETER NAME** | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+--------------------+---------------+--------------------------------+-------------+------------------+
| Resource **[KEY]** | string        | Resource identifier            | N/A         | Temperature      |
+--------------------+---------------+--------------------------------+-------------+------------------+
| ModuleId **[KEY]** | uint8         | Module identifier              |           0 | N/A              |
+--------------------+---------------+--------------------------------+-------------+------------------+
| HighAlarmThreshold | float64       | High alarm threshold value for |      100000 | N/A              |
|                    |               | this PM                        |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| LowWarnThreshold   | float64       | Low warning threshold value    |     -100000 | N/A              |
|                    |               | for this PM                    |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| PMClassBEnable     | bool          | Enable/Disable control for     | true        | N/A              |
|                    |               | CLASS-B PM                     |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| PMClassCEnable     | bool          | Enable/Disable control for     | true        | N/A              |
|                    |               | CLASS-C PM                     |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| HighWarnThreshold  | float64       | High warning threshold value   |      100000 | N/A              |
|                    |               | for this PM                    |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| LowAlarmThreshold  | float64       | Low alarm threshold value for  |     -100000 | N/A              |
|                    |               | this PM                        |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+
| PMClassAEnable     | bool          | Enable/Disable control for     | true        | N/A              |
|                    |               | CLASS-A PM                     |             |                  |
+--------------------+---------------+--------------------------------+-------------+------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/config/AsicGlobalPM
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/AsicGlobalPM/<uuid>
	- UPDATE(PATCH) By Key
		 curl -X PATCH -H 'Content-Type: application/json' -d '{<Model Object as json data>}'  http://device-management-IP:8080/public/v1/config/AsicGlobalPM
	- UPDATE(PATCH) By ID
		 curl -X PATCH -H 'Content-Type: application/json' -d '{<Model Object as json data>}'  http://device-management-IP:8080/public/v1/config/AsicGlobalPM<uuid>


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
		response, error = swtch.getAsicGlobalPM(Resource=resource, ModuleId=moduleid)

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
		response, error = swtch.getAsicGlobalPMById(ObjectId=objectid)

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
		response, error = swtch.getAllAsicGlobalPMs()

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
		response, error = swtch.updateAsicGlobalPM(Resource=resource, ModuleId=moduleid, HighAlarmThreshold=highalarmthreshold, LowWarnThreshold=lowwarnthreshold, PMClassBEnable=pmclassbenable, PMClassCEnable=pmclasscenable, HighWarnThreshold=highwarnthreshold, LowAlarmThreshold=lowalarmthreshold, PMClassAEnable=pmclassaenable)

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
		response, error = swtch.updateAsicGlobalPMById(ObjectId=objectidHighAlarmThreshold=highalarmthreshold, LowWarnThreshold=lowwarnthreshold, PMClassBEnable=pmclassbenable, PMClassCEnable=pmclasscenable, HighWarnThreshold=highwarnthreshold, LowAlarmThreshold=lowalarmthreshold, PMClassAEnable=pmclassaenable)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'
