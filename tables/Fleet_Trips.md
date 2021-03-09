# Table Fleet_Trips

Represents actual trip made by the vehicles. Entity: Fleet_Trips

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Trip_Id](#trip_id)|`uniqueidentifier` `PK`|Trip unique id|
|[Document_Id](#document_id)|`uniqueidentifier` |Trip document data|
|[Vehicle_Set_Id](#vehicle_set_id)|`uniqueidentifier` |The vehicle set for which the trip is reported|
|[Crew_Id](#crew_id)|`uniqueidentifier` |The crew, which operated the vehicle set|
|[Primary_Vehicle_Starting_Mileage](#primary_vehicle_starting_mileage)|`decimal(9, 0)` |Mileage of the primary vehicle in the vehicle set at the begining of the trip. NULL means unknown|
|[Primary_Vehicle_Ending_Mileage](#primary_vehicle_ending_mileage)|`decimal(9, 0)` |Mileage of the primary vehicle in the vehicle set at the ending of the trip. NULL means unknown|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Trip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Set_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Crew_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Primary_Vehicle_Starting_Mileage

| Property | Value |
| - | - |
|Type|decimal(9, 0)|

### Primary_Vehicle_Ending_Mileage

| Property | Value |
| - | - |
|Type|decimal(9, 0)|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


