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


Trip_Segment_Id


Unique trip segment id


Unique trip segment id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Trip_Segment_Id](Fleet_Trip_Segments.md#trip_segment_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Trip_Id


Trip_Id


The trip for which the segment is defined


The trip for which the segment is defined

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Fleet_Trips](Fleet_Trips.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Trip_Id](Fleet_Trip_Segments.md#trip_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Starting_Map_Point_Id


Starting_Map_Point_Id


The starting geographical point of the route segment


The starting geographical point of the route segment

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Geo_Map_Points](Geo_Map_Points.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Starting_Map_Point_Id](Fleet_Trip_Segments.md#starting_map_point_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Starting_Timestamp


Starting_Timestamp


The starting date and time of the travel on the segment


The starting date and time of the travel on the segment

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Starting_Timestamp](Fleet_Trip_Segments.md#starting_timestamp)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Ending_Map_Point_Id


Ending_Map_Point_Id


The ending geographical point of the route segment


The ending geographical point of the route segment

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Geo_Map_Points](Geo_Map_Points.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Ending_Map_Point_Id](Fleet_Trip_Segments.md#ending_map_point_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Ending_Timestamp


Ending_Timestamp


The ending date and time of the travel on the segment


The ending date and time of the travel on the segment

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Ending_Timestamp](Fleet_Trip_Segments.md#ending_timestamp)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Mileage


Mileage


Mileage of the route segment. The mileage is measured in the operational units of the vehicle even when it is not miles or kilometers. NULL means unknown mileage


Mileage of the route segment. The mileage is measured in the operational units of the vehicle even when it is not miles or kilometers. NULL means unknown mileage

| Property | Value |
| - | - |
|Type|decimal(9, 0)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Mileage](Fleet_Trip_Segments.md#mileage)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Notes


Notes


Notes for the segment


Notes for the segment

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Notes](Fleet_Trip_Segments.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Fleet_Trip_Segments](Fleet_Trip_Segments.md).[Row_Version](Fleet_Trip_Segments.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


