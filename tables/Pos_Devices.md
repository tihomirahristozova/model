# Table Pos_Devices

Represents one POS device, attached to a POS terminal. Entity: Pos_Devices (Introduced in version 19.1)

# Aggregate Hierarchy

* [Pos_Terminals](Pos_Terminals.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Pos_Device_Id|`Guid`|`PK`, Readonly||
|Device_Registration_No|`String`||The unique registration number of the device, assigned by the manufacturer. null means the number is unknown or N/A. `Filter(multi eq;like)` |
|Device_Type|`DeviceType`|Allowed: `PAY`, `CSH`, `FIP`, `OTH`|Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other. `Required` `Default("OTH")` `Filter(multi eq)` |
|Electronic_Address|`String`||The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc. `Filter(multi eq;like)` |
|Is_Active|`Boolean`||Indicates whether the device is currently active and can be choosen from drop-downs in new records. `Required` `Default(true)` `Filter(multi eq)` |
|Protocol_Name|`ProtocolName?`|Allowed: `ERPNET_FP`|The name of the protocol, which can be used to communicate with the device. null means that the protocol is unknown and programmatic communication with the device would not be performed. |
|Settings_Json|`String`||Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. null means that there are no settings for this device. |
