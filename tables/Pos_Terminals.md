# Table Pos_Terminals

Represents a POS workplace for 1 person, with all the attached devices. (Not to be confused with Payment Terminal, which is specific POS device). Entity: Pos_Terminals (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Terminal_Id](#pos_terminal_id)|`uniqueidentifier` `PK`||
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |The POS location, where the terminal is located.|
|[Pos_Terminal_Code](#pos_terminal_code)|`nvarchar(16)` |Unique (within the location) code of the POS terminal.|
|[Pos_Terminal_Name](#pos_terminal_name)|`nvarchar(254)` `ML`|The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc.|
|[Is_Active](#is_active)|`bit` |Represents whether the POS terminal is active and can be chosen from drop-downs for new records.|
|[Row_Version](#row_version)|`timestamp` ||
|[Default_Fiscal_Printer_Pos_Device_Id](#default_fiscal_printer_pos_device_id)|`uniqueidentifier` |The POS Fiscal Device which is set by default in documents when the POS Terminal is selected.|

## Columns

### Pos_Terminal_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Terminal_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Pos_Terminal_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Default_Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


