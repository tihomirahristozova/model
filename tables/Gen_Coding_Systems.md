# Table Gen_Coding_Systems

Coding systems categorize additional product codes. Entity: Gen_Coding_Systems

## Summary

| Name | Type | Description |
| - | - | --- |
|[Coding_System_Id](#coding_system_id)|`uniqueidentifier` `PK`||
|[Coding_System_Name](#coding_system_name)|`nvarchar(254)` `ML`||
|[Description](#description)|`nvarchar(2147483647)` ||
|[Default_Measurement_Unit_Id](#default_measurement_unit_id)|`uniqueidentifier` |When not NULL, specifies a measurement unit to be used as default, instead of the products default unit|
|[Is_Unique](#is_unique)|`bit` |1 when the coding system can contain only unique product codes. 0 - duplicate product codes are allowed|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Coding_System_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Coding_System_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Default_Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Unique

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


