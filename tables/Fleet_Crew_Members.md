# Table Fleet_Crew_Members

Contains the memnbers of vehicle crews. Entity: Fleet_Crew_Members

## Owner Tables Hierarchy

* [Fleet_Crews](Fleet_Crews.md)
* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Crew_Member_Id](#crew_member_id)|`uniqueidentifier` `PK`|Id of the crew member|
|[Crew_Id](#crew_id)|`uniqueidentifier` |The crew to which this member belongs|
|[Person_Id](#person_id)|`uniqueidentifier` |The crew member person|
|[Notes](#notes)|`nvarchar(254)` ||
|[Ordinal_Pos](#ordinal_pos)|`int` |Ordinal position. Ordinal_Pos=0 has special meaning - this is the crew leader|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Crew_Member_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Crew_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

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


