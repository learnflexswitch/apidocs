DWDMModuleNwIntfState Object
=============================================================

*state/DWDMModuleNwIntf*
------------------------------------

- Multiple objects of this type can exist in a system.

+---------------------------------+---------------+--------------------------------+-------------+------------------+
|       **PARAMETER NAME**        | **DATA TYPE** |        **DESCRIPTION**         | **DEFAULT** | **VALID VALUES** |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| NwIntfId **[KEY]**              | uint8         | DWDM Module network interface  | N/A         | N/A              |
|                                 |               | identifier                     |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| ModuleId **[KEY]**              | uint8         | DWDM Module identifier         | N/A         | N/A              |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| RxPower                         | float64       | Current RX power for the DWDM  | N/A         | N/A              |
|                                 |               | module network interface       |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| ChanFrequency                   | float64       | Channel frequency              | N/A         | N/A              |
|                                 |               | corresponding to selected      |             |                  |
|                                 |               | channel number for the DWDM    |             |                  |
|                                 |               | module network interface       |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| PRBSRxErrCnt                    | float64       | RX PRBS error count for        | N/A         | N/A              |
|                                 |               | network interface              |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| MinBEROverPMInterval            | float64       | Minimum value of BER over the  | N/A         | N/A              |
|                                 |               | last PM interval for the DWDM  |             |                  |
|                                 |               | module network interface       |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| TxChanGridSpacing               | string        | The channel grid spacing used  | N/A         | N/A              |
|                                 |               | for this network interface in  |             |                  |
|                                 |               | GHz                            |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| UncorrectableFECBlkCntOverPMInt | float64       | Average value of uncorrectable | N/A         | N/A              |
|                                 |               | FEC code block count over the  |             |                  |
|                                 |               | last PM interval               |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| CurrChromDisp                   | int32         | Current RX chromatic           | N/A         | N/A              |
|                                 |               | dispersion for the DWDM module |             |                  |
|                                 |               | network interface              |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| CurrentBER                      | float64       | Current value of BER on the    | N/A         | N/A              |
|                                 |               | DWDM module network interface  |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| MaxBEROverPMInterval            | float64       | Maximum value of BER over the  | N/A         | N/A              |
|                                 |               | last PM interval for the DWDM  |             |                  |
|                                 |               | module network interface       |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| MaxChromDispOverPMInt           | int32         | Current RX chromatic           | N/A         | N/A              |
|                                 |               | dispersion over the last PM    |             |                  |
|                                 |               | interval for the DWDM module   |             |                  |
|                                 |               | network interface              |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| AvgBEROverPMInterval            | float64       | Average value of BER over the  | N/A         | N/A              |
|                                 |               | last PM interval for the DWDM  |             |                  |
|                                 |               | module network interface       |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| AvgChromDispOverPMInt           | int32         | Average RX chromatic           | N/A         | N/A              |
|                                 |               | dispersion over the last PM    |             |                  |
|                                 |               | interval for the DWDM module   |             |                  |
|                                 |               | network interface              |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| CurrUncorrectableFECBlkCnt      | float64       | Current value of uncorrectable | N/A         | N/A              |
|                                 |               | FEC code block count           |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+
| MinChromDispOverPMInt           | int32         | Current RX chromatic           | N/A         | N/A              |
|                                 |               | dispersion over the last PM    |             |                  |
|                                 |               | interval for the DWDM module   |             |                  |
|                                 |               | network interface              |             |                  |
+---------------------------------+---------------+--------------------------------+-------------+------------------+



*FlexSwitch CURL API Supported*
------------------------------------

	- GET By Key
		 curl -X GET -H 'Content-Type: application/json' --header 'Accept: application/json' -d '{<Model Object as json-Data>}' http://device-management-IP:8080/public/v1/state/DWDMModuleNwIntf
	- GET ALL
		 curl -X GET http://device-management-IP:8080/public/v1/state/DWDMModuleNwIntfs?CurrentMarker=<x>&Count=<y>
	- GET By ID
		 curl -X GET http://device-management-IP:8080/public/v1/config/DWDMModuleNwIntfState/<uuid>


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
		response, error = swtch.getDWDMModuleNwIntfState(NwIntfId=nwintfid, ModuleId=moduleid)

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
		response, error = swtch.getDWDMModuleNwIntfStateById(ObjectId=objectid)

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
		response, error = swtch.getAllDWDMModuleNwIntfStates()

		if error != None: #Error not being None implies there is some problem
			print error
		else :
			print 'Success'


