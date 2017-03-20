DWDMModuleClntIntfState Object
=============================================================

*state/DWDMModuleClntIntf*
------------------------------------

- Multiple objects of this type can exist in a system.

+----------------------+---------------+--------------------------------+-------------+------------------+
|  **PARAMETER NAME**  | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+----------------------+---------------+--------------------------------+-------------+------------------+
| ClntIntfId **[KEY]** | uint8         | DWDM Module client interface   | N/A         | N/A              |
|                      |               | identifier                     |             |                  |
+----------------------+---------------+--------------------------------+-------------+------------------+
| ModuleId **[KEY]**   | uint8         | DWDM Module identifier         | N/A         | N/A              |
+----------------------+---------------+--------------------------------+-------------+------------------+
| PRBSTxErrCntLane1    | float64       | Client interface host lane 1   | N/A         | N/A              |
|                      |               | PRBS TX Error count            |             |                  |
+----------------------+---------------+--------------------------------+-------------+------------------+
| PRBSTxErrCntLane2    | float64       | Client interface host lane 2   | N/A         | N/A              |
|                      |               | PRBS TX Error count            |             |                  |
+----------------------+---------------+--------------------------------+-------------+------------------+
| PRBSTxErrCntLane3    | float64       | Client interface host lane 3   | N/A         | N/A              |
|                      |               | PRBS TX Error count            |             |                  |
+----------------------+---------------+--------------------------------+-------------+------------------+
| PRBSTxErrCntLane0    | float64       | Client interface host lane 0   | N/A         | N/A              |
|                      |               | PRBS TX Error count            |             |                  |
+----------------------+---------------+--------------------------------+-------------+------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/DWDMModuleClntIntf
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/DWDMModuleClntIntfs?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/DWDMModuleClntIntfState/<uuid>


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
		response, error = swtch.getDWDMModuleClntIntfState(ClntIntfId=clntintfid, ModuleId=moduleid)

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
		response, error = swtch.getDWDMModuleClntIntfStateById(ObjectId=objectid)

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
		response, error = swtch.getAllDWDMModuleClntIntfStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


