Qsfp Object
=============================================================

*config/Qsfp*
------------------------------------

- Multiple objects of this type can exist in a system.

+--------------------------+---------------+--------------------------------+-------------+------------------+
|    **PARAMETER NAME**    | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| QsfpId **[KEY]**         | int32         | Qsfp Id                        | N/A         | N/A              |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| LowerWarningTemperature  | float64       | Lower Warning temperature      | N/A         | N/A              |
|                          |               | threshold for TCA              |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| PMClassAAdminState       | string        | PM Class-A Admin State         | Disable     | Enable, Disable  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| PMClassCAdminState       | string        | PM Class-C Admin State         | Disable     | Enable, Disable  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| AdminState               | string        | Enable/Disable                 | Disable     | Enable, Disable  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| HigherWarningTemperature | float64       | Higher Warning temperature     | N/A         | N/A              |
|                          |               | threshold for TCA              |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| LowerAlarmTemperature    | float64       | Lower Alarm temperature        | N/A         | N/A              |
|                          |               | threshold for TCA              |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| LowerAlarmVoltage        | float64       | Lower Alarm Voltage threshold  | N/A         | N/A              |
|                          |               | for TCA                        |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| PMClassBAdminState       | string        | PM Class-B Admin State         | Disable     | Enable, Disable  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| HigherAlarmTemperature   | float64       | Higher Alarm temperature       | N/A         | N/A              |
|                          |               | threshold for TCA              |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| HigherAlarmVoltage       | float64       | Higher Alarm Voltage threshold | N/A         | N/A              |
|                          |               | for TCA                        |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| HigherWarningVoltage     | float64       | Higher Warning Voltage         | N/A         | N/A              |
|                          |               | threshold for TCA              |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+
| LowerWarningVoltage      | float64       | Lower Warning Voltage          | N/A         | N/A              |
|                          |               | threshold for TCA              |             |                  |
+--------------------------+---------------+--------------------------------+-------------+------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/config/Qsfp
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/Qsfp/<uuid>
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/config/Qsfps?CurrentMarker=<x>&Count=<y>
	- UPDATE(PATCH) By Key
		 curl -X PATCH -H 'Content-Type: application/json' -d '{<Model Object as json data>}'  http://device-management-IP:8080/public/v1/config/Qsfp
	- UPDATE(PATCH) By ID
		 curl -X PATCH -H 'Content-Type: application/json' -d '{<Model Object as json data>}'  http://device-management-IP:8080/public/v1/config/Qsfp<uuid>


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
		response, error = swtch.getQsfp(QsfpId=qsfpid)

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
		response, error = swtch.getQsfpById(ObjectId=objectid)

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
		response, error = swtch.getAllQsfps()

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
		response, error = swtch.updateQsfp(QsfpId=qsfpid, LowerWarningTemperature=lowerwarningtemperature, PMClassAAdminState=pmclassaadminstate, PMClassCAdminState=pmclasscadminstate, AdminState=adminstate, HigherWarningTemperature=higherwarningtemperature, LowerAlarmTemperature=loweralarmtemperature, LowerAlarmVoltage=loweralarmvoltage, PMClassBAdminState=pmclassbadminstate, HigherAlarmTemperature=higheralarmtemperature, HigherAlarmVoltage=higheralarmvoltage, HigherWarningVoltage=higherwarningvoltage, LowerWarningVoltage=lowerwarningvoltage)

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
		response, error = swtch.updateQsfpById(ObjectId=objectidLowerWarningTemperature=lowerwarningtemperature, PMClassAAdminState=pmclassaadminstate, PMClassCAdminState=pmclasscadminstate, AdminState=adminstate, HigherWarningTemperature=higherwarningtemperature, LowerAlarmTemperature=loweralarmtemperature, LowerAlarmVoltage=loweralarmvoltage, PMClassBAdminState=pmclassbadminstate, HigherAlarmTemperature=higheralarmtemperature, HigherAlarmVoltage=higheralarmvoltage, HigherWarningVoltage=higherwarningvoltage, LowerWarningVoltage=lowerwarningvoltage)

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'
