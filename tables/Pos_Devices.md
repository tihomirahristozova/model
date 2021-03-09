# Table Pos_Devices

Represents one POS device, attached to a POS terminal. Entity: Pos_Devices (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Pos_Terminals](Pos_Terminals.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Device_Id](#pos_device_id)|`uniqueidentifier` `PK`||
|[Pos_Terminal_Id](#pos_terminal_id)|`uniqueidentifier` |The POS terminal, to which this device is attached.|
|[Device_Type](#device_type)|`nvarchar(3)` Allowed: `PAY`, `CSH`, `FIP`, `OTH`|Type of the POS device. PAY=Payment Terminal; CSH=Cash Drawer; FIP=Fiscal Printer; OTH=Other.|
|[Device_Registration_No](#device_registration_no)|`nvarchar(32)` |The unique registration number of the device, assigned by the manufacturer. NULL means the number is unknown or N/A.|
|[Protocol_Name](#protocol_name)|`nvarchar(32)` Allowed: `ERPNET_FP`|The name of the protocol, which can be used to communicate with the device. NULL means that the protocol is unknown and programmatic communication with the device would not be performed.|
|[Electronic_Address](#electronic_address)|`nvarchar(254)` |The absolute address (Internet or other) which can be used for electronic communication with the device. The address should contain communication protocol/type, colon, space, then the actual address. Addresses, which are local to a specific computer, should also include the computer name. For example: "COM: PC_WORK1:COM1", "HTTP: https://<addr>", etc.|
|[Settings_Json](#settings_json)|`nvarchar(2147483647)` |Settings and operator access codes for the POS device. The data is stored as Json, encrypted for the current application server instance. NULL means that there are no settings for this device.|
|[Is_Active](#is_active)|`bit` |Indicates whether the device is currently active and can be choosen from drop-downs in new records.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Terminal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Device_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Device_Registration_No

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Protocol_Name

| Property | Value |
| - | - |
|Type|nvarchar(32)|

### Electronic_Address

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Settings_Json

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


