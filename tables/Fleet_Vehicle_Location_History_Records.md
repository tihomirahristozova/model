# Table Fleet_Vehicle_Location_History_Records

Stores information about vehicle locations. Entity: Fleet_Vehicle_Location_History_Records

## Summary

| Name | Type | Description |
| - | - | --- |
|[Vehicle_Location_History_Record_Id](#vehicle_location_history_record_id)|`uniqueidentifier` `PK`||
|[Vehicle_Id](#vehicle_id)|`uniqueidentifier` |The vehicle, whose location is being stored.|
|[Time](#time)|`datetime` |The time, for which the location is stored.|
|[Latitude](#latitude)|`decimal(10, 7)` |Latitude of the vehicle at the specified time. Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90].|
|[Longitude](#longitude)|`decimal(10, 7)` |Longitude of the vehicle at the specified time. Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180].|
|[Current_Speed_KmH](#current_speed_kmh)|`int` |The current speed of the vehicle in km/h. NULL means the speed is unknown.|

## Columns

### Vehicle_Location_History_Record_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Vehicle_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Time

| Property | Value |
| - | - |
|Type|datetime|

### Latitude

| Property | Value |
| - | - |
|Type|decimal(10, 7)|

### Longitude

| Property | Value |
| - | - |
|Type|decimal(10, 7)|

### Current_Speed_KmH

| Property | Value |
| - | - |
|Type|int|


