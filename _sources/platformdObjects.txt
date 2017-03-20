PLATFORMD Model Objects
============================================

*state/PlatformMgmtDevice*
------------------------------------

- **DeviceName**
	- **Data Type**: string
	- **Description**: Device Name.
	- This parameter is key element.
	- **Default**: BMC
- **MemoryUsage**
	- **Data Type**: string
	- **Description**: Memory Usage.
- **ResetReason**
	- **Data Type**: string
	- **Description**: Reset Reason.
- **Uptime**
	- **Data Type**: string
	- **Description**: Uptime and load description.
- **Version**
	- **Data Type**: string
	- **Description**: Version.
- **CPUUsage**
	- **Data Type**: string
	- **Description**: CPU Usage.
- **Description**
	- **Data Type**: string
	- **Description**: Platform Description.


*state/TemperatureSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Temperature Sensor Name.
	- This parameter is key element.
- **CurrentTemperature**
	- **Data Type**: float64
	- **Description**: Current Temperature Value.


*state/TemperatureSensorPMData*
------------------------------------

- **Class**
	- **Data Type**: string
	- **Description**: Class of PM Data.
	- This parameter is key element.
	- **Default**: CLASS-A
	- **Possible Values**: CLASS-A, CLASS-B, CLASS-B
- **Name**
	- **Data Type**: string
	- **Description**: Temperature Sensor Name.
	- This parameter is key element.
- **Data**
	- **Data Type**: TemperatureSensorPMData
	- **Description**: .


*config/TemperatureSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Temperature Sensor Name.
	- This parameter is key element.
- **PMClassAAdminState**
	- **Data Type**: string
	- **Description**: PM Class-A Admin State.
	- **Default**: Enable
- **PMClassCAdminState**
	- **Data Type**: string
	- **Description**: PM Class-C Admin State.
	- **Default**: Enable
- **HigherAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Higher Alarm Threshold for TCA.
- **LowerAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Lower Alarm Threshold for TCA.
- **LowerWarningThreshold**
	- **Data Type**: float64
	- **Description**: Lower Warning Threshold for TCA.
- **PMClassBAdminState**
	- **Data Type**: string
	- **Description**: PM Class-B Admin State.
	- **Default**: Enable
- **AdminState**
	- **Data Type**: string
	- **Description**: Enable/Disable.
	- **Default**: Enable
- **HigherWarningThreshold**
	- **Data Type**: float64
	- **Description**: Higher Warning Threshold for TCA.


*state/PowerConverterSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Power Converter Sensor Name.
	- This parameter is key element.
- **CurrentPower**
	- **Data Type**: float64
	- **Description**: Current Output Power Value.


*config/FanSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Fan Sensor Name.
	- This parameter is key element.
- **HigherWarningThreshold**
	- **Data Type**: int32
	- **Description**: Higher Warning Threshold for TCA.
- **LowerAlarmThreshold**
	- **Data Type**: int32
	- **Description**: Lower Alarm Threshold for TCA.
- **LowerWarningThreshold**
	- **Data Type**: int32
	- **Description**: Lower Warning Threshold for TCA.
- **PMClassAAdminState**
	- **Data Type**: string
	- **Description**: PM Class-A Admin State.
	- **Default**: Enable
- **AdminState**
	- **Data Type**: string
	- **Description**: Enable/Disable.
	- **Default**: Enable
- **HigherAlarmThreshold**
	- **Data Type**: int32
	- **Description**: Higher Alarm Threshold for TCA.
- **PMClassBAdminState**
	- **Data Type**: string
	- **Description**: PM Class-B Admin State.
	- **Default**: Enable
- **PMClassCAdminState**
	- **Data Type**: string
	- **Description**: PM Class-C Admin State.
	- **Default**: Enable


*state/VoltageSensorPMData*
------------------------------------

- **Class**
	- **Data Type**: string
	- **Description**: Class of PM Data.
	- This parameter is key element.
	- **Default**: CLASS-A
	- **Possible Values**: CLASS-A, CLASS-B, CLASS-B
- **Name**
	- **Data Type**: string
	- **Description**: Voltage Sensor Name.
	- This parameter is key element.
- **Data**
	- **Data Type**: VoltageSensorPMData
	- **Description**: .


*state/FanSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Fan Sensor Name.
	- This parameter is key element.
- **CurrentSpeed**
	- **Data Type**: int32
	- **Description**: Fan Current Speed.


*config/QsfpChannel*
------------------------------------

- **ChannelNum**
	- **Data Type**: int32
	- **Description**: Qsfp Channel Number.
	- This parameter is key element.
- **QsfpId**
	- **Data Type**: int32
	- **Description**: Qsfp Id.
	- This parameter is key element.
- **HigherAlarmTXPower**
	- **Data Type**: float64
	- **Description**: Higher Alarm Rx power for TCA.
- **HigherWarningRXPower**
	- **Data Type**: float64
	- **Description**: Higher Warning Rx power Threshold for TCA.
- **LowerAlarmTXPower**
	- **Data Type**: float64
	- **Description**: Lower Alarm Rx power for TCA.
- **LowerWarningRXPower**
	- **Data Type**: float64
	- **Description**: Lower Warning Rx power Threshold for TCA.
- **LowerWarningTXPower**
	- **Data Type**: float64
	- **Description**: Lower Warning Rx power for TCA.
- **HigherWarningTXBias**
	- **Data Type**: float64
	- **Description**: Higher Warning Tx Current Bias for TCA.
- **HigherWarningTXPower**
	- **Data Type**: float64
	- **Description**: Higher Warning Rx power for TCA.
- **LowerAlarmTXBias**
	- **Data Type**: float64
	- **Description**: Lower Alarm Tx Current Bias for TCA.
- **LowerWarningTXBias**
	- **Data Type**: float64
	- **Description**: Lower Warning Tx Current Bias for TCA.
- **HigherAlarmTXBias**
	- **Data Type**: float64
	- **Description**: Higher Alarm Tx Current Bias for TCA.
- **LowerAlarmRXPower**
	- **Data Type**: float64
	- **Description**: Lower Alarm Rx power Threshold for TCA.
- **PMClassAAdminState**
	- **Data Type**: string
	- **Description**: PM Class-A Admin State.
	- **Default**: Disable
- **PMClassBAdminState**
	- **Data Type**: string
	- **Description**: PM Class-B Admin State.
	- **Default**: Disable
- **PMClassCAdminState**
	- **Data Type**: string
	- **Description**: PM Class-C Admin State.
	- **Default**: Disable
- **AdminState**
	- **Data Type**: string
	- **Description**: Enable/Disable.
	- **Default**: Disable
- **HigherAlarmRXPower**
	- **Data Type**: float64
	- **Description**: Higher Alarm Rx power Threshold for TCA.


*config/Qsfp*
------------------------------------

- **QsfpId**
	- **Data Type**: int32
	- **Description**: Qsfp Id.
	- This parameter is key element.
- **HigherAlarmVoltage**
	- **Data Type**: float64
	- **Description**: Higher Alarm Voltage threshold for TCA.
- **HigherWarningVoltage**
	- **Data Type**: float64
	- **Description**: Higher Warning Voltage threshold for TCA.
- **LowerAlarmTemperature**
	- **Data Type**: float64
	- **Description**: Lower Alarm temperature threshold for TCA.
- **LowerWarningVoltage**
	- **Data Type**: float64
	- **Description**: Lower Warning Voltage threshold for TCA.
- **PMClassAAdminState**
	- **Data Type**: string
	- **Description**: PM Class-A Admin State.
	- **Default**: Disable
- **PMClassBAdminState**
	- **Data Type**: string
	- **Description**: PM Class-B Admin State.
	- **Default**: Disable
- **AdminState**
	- **Data Type**: string
	- **Description**: Enable/Disable.
	- **Default**: Disable
- **HigherAlarmTemperature**
	- **Data Type**: float64
	- **Description**: Higher Alarm temperature threshold for TCA.
- **HigherWarningTemperature**
	- **Data Type**: float64
	- **Description**: Higher Warning temperature threshold for TCA.
- **LowerAlarmVoltage**
	- **Data Type**: float64
	- **Description**: Lower Alarm Voltage threshold for TCA.
- **LowerWarningTemperature**
	- **Data Type**: float64
	- **Description**: Lower Warning temperature threshold for TCA.
- **PMClassCAdminState**
	- **Data Type**: string
	- **Description**: PM Class-C Admin State.
	- **Default**: Disable


*state/QsfpChannel*
------------------------------------

- **QsfpId**
	- **Data Type**: int32
	- **Description**: QSFP Id.
	- This parameter is key element.
- **ChannelNum**
	- **Data Type**: int32
	- **Description**: Qsfp Channel Number.
	- This parameter is key element.
- **RXPower**
	- **Data Type**: float64
	- **Description**: Rx power on channel 1.
- **TXBias**
	- **Data Type**: float64
	- **Description**: Tx Current Bias on channel 1.
- **TXPower**
	- **Data Type**: float64
	- **Description**: Rx power on channel 1.
- **Present**
	- **Data Type**: bool
	- **Description**: Present or Not Value.


*state/FanSensorPMData*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Fan Sensor Name.
	- This parameter is key element.
- **Class**
	- **Data Type**: string
	- **Description**: Class of PM Data.
	- This parameter is key element.
	- **Default**: CLASS-A
	- **Possible Values**: CLASS-A, CLASS-B, CLASS-B
- **Data**
	- **Data Type**: FanSensorPMData
	- **Description**: .


*state/QsfpPMData*
------------------------------------

- **Class**
	- **Data Type**: string
	- **Description**: Class of PM Data.
	- This parameter is key element.
	- **Default**: CLASS-A
	- **Possible Values**: CLASS-A, CLASS-B, CLASS-B
- **QsfpId**
	- **Data Type**: int32
	- **Description**: QSFP Id.
	- This parameter is key element.
- **Resource**
	- **Data Type**: string
	- **Description**: QSFP PM Resource Name.
	- This parameter is key element.
- **Data**
	- **Data Type**: QsfpPMData
	- **Description**: .


*state/QsfpChannelPMData*
------------------------------------

- **QsfpId**
	- **Data Type**: int32
	- **Description**: QSFP Id.
	- This parameter is key element.
- **Resource**
	- **Data Type**: string
	- **Description**: QSFP PM Resource Name.
	- This parameter is key element.
- **ChannelNum**
	- **Data Type**: int32
	- **Description**: Qsfp Channel Number.
	- This parameter is key element.
- **Class**
	- **Data Type**: string
	- **Description**: Class of PM Data.
	- This parameter is key element.
	- **Default**: CLASS-A
	- **Possible Values**: CLASS-A, CLASS-B, CLASS-B
- **Data**
	- **Data Type**: QsfpChannelPMData
	- **Description**: .


*state/Qsfp*
------------------------------------

- **QsfpId**
	- **Data Type**: int32
	- **Description**: QSFP Id.
	- This parameter is key element.
- **DataCode**
	- **Data Type**: string
	- **Description**: Data Code.
- **VendorName**
	- **Data Type**: string
	- **Description**: Vendor Name.
- **VendorSerialNumber**
	- **Data Type**: string
	- **Description**: Vendor Serial Number.
- **VendorPartNumber**
	- **Data Type**: string
	- **Description**: Vendor Part Number.
- **VendorRevision**
	- **Data Type**: string
	- **Description**: Vendor Revision.
- **Voltage**
	- **Data Type**: float64
	- **Description**: Current Voltage.
- **Present**
	- **Data Type**: bool
	- **Description**: Present or Not Value.
- **Temperature**
	- **Data Type**: float64
	- **Description**: Current temperature.
- **VendorOUI**
	- **Data Type**: string
	- **Description**: Vendor OUI.


*state/VoltageSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Voltage Sensor Name.
	- This parameter is key element.
- **CurrentVoltage**
	- **Data Type**: float64
	- **Description**: Current Voltage Value.


*config/PowerConverterSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Power Converter Sensor Name.
	- This parameter is key element.
- **PMClassCAdminState**
	- **Data Type**: string
	- **Description**: PM Class-C Admin State.
	- **Default**: Enable
- **AdminState**
	- **Data Type**: string
	- **Description**: Enable/Disable.
	- **Default**: Enable
- **LowerAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Lower Alarm Threshold for TCA.
- **LowerWarningThreshold**
	- **Data Type**: float64
	- **Description**: Lower Warning Threshold for TCA.
- **PMClassBAdminState**
	- **Data Type**: string
	- **Description**: PM Class-B Admin State.
	- **Default**: Enable
- **HigherAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Higher Alarm Threshold for TCA.
- **HigherWarningThreshold**
	- **Data Type**: float64
	- **Description**: Higher Warning Threshold for TCA.
- **PMClassAAdminState**
	- **Data Type**: string
	- **Description**: PM Class-A Admin State.
	- **Default**: Enable


*state/PowerConverterSensorPMData*
------------------------------------

- **Class**
	- **Data Type**: string
	- **Description**: Class of PM Data.
	- This parameter is key element.
	- **Default**: CLASS-A
	- **Possible Values**: CLASS-A, CLASS-B, CLASS-B
- **Name**
	- **Data Type**: string
	- **Description**: Power Converter Sensor Name.
	- This parameter is key element.
- **Data**
	- **Data Type**: PowerConverterSensorPMData
	- **Description**: .


*config/VoltageSensor*
------------------------------------

- **Name**
	- **Data Type**: string
	- **Description**: Voltage Sensor Name.
	- This parameter is key element.
- **LowerAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Lower Alarm Threshold for TCA.
- **PMClassBAdminState**
	- **Data Type**: string
	- **Description**: PM Class-B Admin State.
	- **Default**: Enable
- **HigherWarningThreshold**
	- **Data Type**: float64
	- **Description**: Higher Warning Threshold for TCA.
- **HigherAlarmThreshold**
	- **Data Type**: float64
	- **Description**: Higher Alarm Threshold for TCA.
- **LowerWarningThreshold**
	- **Data Type**: float64
	- **Description**: Lower Warning Threshold for TCA.
- **PMClassAAdminState**
	- **Data Type**: string
	- **Description**: PM Class-A Admin State.
	- **Default**: Enable
- **PMClassCAdminState**
	- **Data Type**: string
	- **Description**: PM Class-C Admin State.
	- **Default**: Enable
- **AdminState**
	- **Data Type**: string
	- **Description**: Enable/Disable.
	- **Default**: Enable


