# Table Gen_Measurement_Units

Contains all measurement units, grouped in categories. Each category has one base unit (with ratio 1/1) and unlimited number of derived units with fixed ratio to the base unit. Entity: Gen_Measurement_Units

## Owner Tables Hierarchy

* [Gen_Measurement_Categories](Gen_Measurement_Categories.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique measurement unit Id|
|[Measurement_Category_Id](#measurement_category_id)|`uniqueidentifier` |Base measurement category Id|
|[Measurement_Unit_Name](#measurement_unit_name)|`nvarchar(64)` `ML`|Name of the measurement unit|
|[Multiplier](#multiplier)|`decimal(9, 3)` |Multiplier of the relative value of the measurement unit against other units (multiplier when converting to base)|
|[Divisor](#divisor)|`decimal(9, 3)` |Divisor of the relative value of the measurement unit against other units (divisor when converting to base)|
|[Is_Default_Unit](#is_default_unit)|`bit` |1 if this measurement unit is the default measurement unit within the category. There can be only one default measurement unit within a category|
|[System_Unit](#system_unit)|`nvarchar(1)` Allowed: `G`, `H`, `L`, `N`, `P`, `V`, `W`, `T`|Not NULL only when this is one of the system measurement units. N=NetKG; G=GrossKG; V=VolumeL; H=HeightM; W=WidthM, L=LengthM, P=Piece, T=TimeH|
|[Measurement_Unit_Code](#measurement_unit_code)|`nvarchar(16)` |When not null, contains unique measurement unit code.|
|[Description](#description)|`nvarchar(2147483647)` `ML`|Full multi-language description of the measurement unit.|
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
|Type|nvarchar(64)|

### Multiplier

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Divisor

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Is_Default_Unit

| Property | Value |
| - | - |
|Type|bit|

### System_Unit

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Measurement_Unit_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


