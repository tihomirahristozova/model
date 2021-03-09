# Table Log_Transportation_Vehicles

A vehicle, which is used for transportation. One actual vehicle might be defined multiple times as transportation vehicle - for different modes of transportation or cargo types. Entity: Log_Transportation_Vehicles

## Owner Tables Hierarchy

* [Fleet_Vehicles](Fleet_Vehicles.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transportation_Vehicle_Id](#transportation_vehicle_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company to which the transportation vehicle will be bound.|
|[Code](#code)|`nvarchar(16)` |The unique code (or call sign) of this transportation vehicle.|
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The definition of the base vehicle.|
|[Transportation_Mode_Id](#transportation_mode_id)|`uniqueidentifier` |The mode of transportation provided by this transportation vehicle. The same base vehicle might be used for more than one mode.|
|[Cargo_Type_Id](#cargo_type_id)|`uniqueidentifier` |The cargo type supported by this transportation vehicle.|
|[Max_Cargo_Weight_Kg](#max_cargo_weight_kg)|`int` |The maximum weight of the cargo (in kg), which can be transported. NULL when this is unknown and no limit should be enforced.|
|[Max_Pallets_Count](#max_pallets_count)|`int` |The maximum number of pallets, which can be transported by the vehicle. NULL when this is unknown and no limit should be enforced.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transportation_Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transportation_Mode_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cargo_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Max_Cargo_Weight_Kg

| Property | Value |
| - | - |
|Type|int|

### Max_Pallets_Count

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


