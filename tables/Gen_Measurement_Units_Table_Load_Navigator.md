# Query Gen_Measurement_Units_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Measurement_Category_Id](#measurement_category_id)|`uniqueidentifier` ||
|[Measurement_Unit_Name](#measurement_unit_name)|`nvarchar` `ML`||
|[Multiplier](#multiplier)|`decimal(0, 0)` ||
|[Divisor](#divisor)|`decimal(0, 0)` ||
|[Is_Default_Unit](#is_default_unit)|`bit` ||
|[System_Unit](#system_unit)|`nvarchar` Allowed: `G`, `H`, `L`, `N`, `P`, `V`, `W`, `T`||
|[Measurement_Unit_Code](#measurement_unit_code)|`nvarchar` |When not null, contains unique measurement unit code.|
|[Description](#description)|`nvarchar` `ML`|Full multi-language description of the measurement unit.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Measurement_Unit_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Multiplier

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Divisor

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Is_Default_Unit

| Property | Value |
| - | - |
|Type|bit|

### System_Unit

| Property | Value |
| - | - |
|Type|nvarchar|

### Measurement_Unit_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


