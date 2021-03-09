# Table Fleet_Vehicle_Sets

Represents sets of vehicles, which can travel together. Entity: Fleet_Vehicle_Sets

## Owner Tables Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Set_Id](#vehicle_set_id)|`uniqueidentifier` `PK`|Id of the vehicle set (composition of vehicles, used together)|
|[Vehicle_Set_Name](#vehicle_set_name)|`nvarchar(128)` `ML`|Name of the vehicle set (Multilanguage)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company operating the vehicle set|
|[Active](#active)|`bit` |1 if the vehicle set is active for choosing; 0 - otherwise|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Vehicle_Set_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Set_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


