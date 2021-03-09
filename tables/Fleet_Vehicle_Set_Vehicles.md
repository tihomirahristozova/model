# Table Fleet_Vehicle_Set_Vehicles

Contains lists of vehicles in the vehicle sets. Entity: Fleet_Vehicle_Set_Vehicles

## Owner Tables Hierarchy

* [Fleet_Vehicle_Sets](Fleet_Vehicle_Sets.md)
* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Set_Vehicle_Id](#vehicle_set_vehicle_id)|`uniqueidentifier` `PK`||
|[Vehicle_Set_Id](#vehicle_set_id)|`uniqueidentifier` ||
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The Vehicle which is part of the vehicle set|
|[Notes](#notes)|`nvarchar(254)` ||
|[Ordinal_Pos](#ordinal_pos)|`int` |Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Vehicle_Set_Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Set_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Ordinal_Pos

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


