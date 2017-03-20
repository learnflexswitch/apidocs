QsfpChannelPMDataState Object
=============================================================

*state/QsfpChannelPMData*
------------------------------------

- Multiple objects of this type can exist in a system.

+----------------------+-------------------+-----------------------+-------------+---------------------------+
|  **PARAMETER NAME**  |   **DATA TYPE**   |    **DESCRIPTION**    | **DEFAULT** |     **VALID VALUES**      |
+----------------------+-------------------+-----------------------+-------------+---------------------------+
| QsfpId **[KEY]**     | int32             | QSFP Id               | N/A         | N/A                       |
+----------------------+-------------------+-----------------------+-------------+---------------------------+
| Resource **[KEY]**   | string            | QSFP PM Resource Name | N/A         | N/A                       |
+----------------------+-------------------+-----------------------+-------------+---------------------------+
| ChannelNum **[KEY]** | int32             | Qsfp Channel Number   | N/A         | N/A                       |
+----------------------+-------------------+-----------------------+-------------+---------------------------+
| Class **[KEY]**      | string            | Class of PM Data      | CLASS-A     | CLASS-A, CLASS-B, CLASS-B |
+----------------------+-------------------+-----------------------+-------------+---------------------------+
| Data                 | QsfpChannelPMData |                       | N/A         | N/A                       |
+----------------------+-------------------+-----------------------+-------------+---------------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/QsfpChannelPMData
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/QsfpChannelPMDatas?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/QsfpChannelPMDataState/<uuid>


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
		response, error = swtch.getQsfpChannelPMDataState(QsfpId=qsfpid, Resource=resource, ChannelNum=channelnum, Class=class)

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
		response, error = swtch.getQsfpChannelPMDataStateById(ObjectId=objectid)

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
		response, error = swtch.getAllQsfpChannelPMDataStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


