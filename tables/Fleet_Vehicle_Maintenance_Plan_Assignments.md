# Table Fleet_Vehicle_Maintenance_Plan_Assignments

Represents assignment of a maintenance plan to a vehicle. Entity: Fleet_Vehicle_Maintenance_Plan_Assignments

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Maintenance_Plan_Assignment_Id](#vehicle_maintenance_plan_assignment_id)|`uniqueidentifier` `PK`||
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The vehicle, to which a periodic maintenance plan is assigned.|
|[Maintenance_Plan_Id](#maintenance_plan_id)|`uniqueidentifier` |The assigned periodic maintenance type.|
|[Starting_Date](#starting_date)|`date` |The date on which the periodic maintenance should start.|
|[Last_Maintenance_Mileage_Km](#last_maintenance_mileage_km)|`int` |The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check.|
|[Last_Maintenance_Trip_Count](#last_maintenance_trip_count)|`int` |The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check.|
|[Is_Active](#is_active)|`bit` |Specifies whether the plan is active.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Vehicle_Maintenance_Plan_Assignment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Plan_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Starting_Date

| Property | Value |
| - | - |
|Type|date|

### Last_Maintenance_Mileage_Km

| Property | Value |
| - | - |
|Type|int|

### Last_Maintenance_Trip_Count

| Property | Value |
| - | - |
|Type|int|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


