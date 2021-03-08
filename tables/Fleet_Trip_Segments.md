# Table Fleet_Trip_Segments

Represents the segments which comprise the route of the trips. Entity: Fleet_Trip_Segments

# Aggregate Hierarchy

* [Fleet_Trips](Fleet_Trips.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Trip_Segment_Id|`Guid`|`PK`, Readonly||
|Ending_Timestamp|`DateTime?`||The ending date and time of the travel on the segment. |
|Mileage|`Decimal?`||Mileage of the route segment. The mileage is measured in the operational units of the vehicle even when it is not miles or kilometers. null means unknown mileage. |
|Notes|`String`||Notes for the segment. |
|Starting_Timestamp|`DateTime`||The starting date and time of the travel on the segment. `Required` |
