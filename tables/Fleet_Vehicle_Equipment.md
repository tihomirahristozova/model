# Table Fleet_Vehicle_Equipment

Contains the actual and history of equipment, installed on the vehicles. Entity: Fleet_Vehicle_Equipment

## Owner Tables Hierarchy

* [Fleet_Vehicles](Fleet_Vehicles.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Equipment_Id](#vehicle_equipment_id)|`uniqueidentifier` `PK`||
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The vehicle that is holding the equipment|
|[Equipment_Type_Id](#equipment_type_id)|`uniqueidentifier` |The type of equipment installed on the vehicle|
|[Quantity](#quantity)|`int` |Quantity of the equipment|
|[Start_Date](#start_date)|`date` |The installation date of the equipment|
|[End_Date](#end_date)|`date` |The date when the equipment was removed. NULL when the equipment is still installed on the vehicle|
|[Notes](#notes)|`nvarchar(2147483647)` |Notes for the installed equipment|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Vehicle_Equipment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Equipment_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|int|

### Start_Date

| Property | Value |
| - | - |
|Type|date|

### End_Date

| Property | Value |
| - | - |
|Type|date|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


