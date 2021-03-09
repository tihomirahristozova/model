# Table Log_Logistic_Unit_Types

Types of logistic units, like EU-PALLET, 40x40 pallet, ISO container, etc. Entity: Log_Logistic_Unit_Types (Introduced in version 21.1.0.77)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Logistic_Unit_Type_Id](#logistic_unit_type_id)|`uniqueidentifier` `PK`||
|[Code](#code)|`nvarchar(16)` |Unique code of the logistic unit type. Used for display and selection purposes. Can contain only EN letters and numbers.|
|[Name](#name)|`nvarchar(254)` `ML`|Multi-language name of the logistic unit type.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Logistic_Unit_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


