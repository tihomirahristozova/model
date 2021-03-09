# Query Pos_Terminals_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Terminal_Id](#pos_terminal_id)|`uniqueidentifier` `PK`||
|[Pos_Location_Id](#pos_location_id)|`uniqueidentifier` |The POS location, where the terminal is located.|
|[Pos_Terminal_Code](#pos_terminal_code)|`nvarchar` |Unique (within the location) code of the POS terminal.|
|[Pos_Terminal_Name](#pos_terminal_name)|`nvarchar` `ML`|The multi-language name of the terminal, like "Cash 1", "Self-checkout 5", etc.|
|[Is_Active](#is_active)|`bit` |Represents whether the POS terminal is active and can be chosen from drop-downs for new records.|
|[Default_Fiscal_Printer_Pos_Device_Id](#default_fiscal_printer_pos_device_id)|`uniqueidentifier` |The POS Fiscal Device which is set by default in documents when the POS Terminal is selected.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Enterprise_Company_Location_Id](#enterprise_company_location_id)|`uniqueidentifier` |The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location.|
|[Pos_Location_Code](#pos_location_code)|`nvarchar` |Unique (with the enterprise company) code of this POS location.|
|[Pos_Location_Is_Active](#pos_location_is_active)|`bit` |Indicates whether the POS location is currently active and can be chosen in drop-downs, etc.|

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
|Type|nvarchar|

### Pos_Terminal_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Default_Fiscal_Printer_Pos_Device_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Location_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Pos_Location_Is_Active

| Property | Value |
| - | - |
|Type|bit|


