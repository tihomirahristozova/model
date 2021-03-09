# Table Fleet_Trip_Segments

Represents the segments which comprise the route of the trips. Entity: Fleet_Trip_Segments

## Owner Tables Hierarchy

* [Fleet_Trips](Fleet_Trips.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Trip_Segment_Id](#trip_segment_id)|`uniqueidentifier` `PK`|Unique trip segment id|
|[Trip_Id](#trip_id)|`uniqueidentifier` |The trip for which the segment is defined|
|[Starting_Map_Point_Id](#starting_map_point_id)|`uniqueidentifier` |The starting geographical point of the route segment|
|[Starting_Timestamp](#starting_timestamp)|`datetime` |The starting date and time of the travel on the segment|
|[Ending_Map_Point_Id](#ending_map_point_id)|`uniqueidentifier` |The ending geographical point of the route segment|
|[Ending_Timestamp](#ending_timestamp)|`datetime` |The ending date and time of the travel on the segment|
|[Mileage](#mileage)|`decimal(9, 0)` |Mileage of the route segment. The mileage is measured in the operational units of the vehicle even when it is not miles or kilometers. NULL means unknown mileage|
|[Notes](#notes)|`nvarchar(254)` |Notes for the segment|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Trip_Segment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Trip_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Starting_Map_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Starting_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Ending_Map_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ending_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Mileage

| Property | Value |
| - | - |
|Type|decimal(9, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


