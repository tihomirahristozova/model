# Table Geo_Map_Points

Geographical map points are used as points of interest on the map. They are used for routing and other purposes. The points of interest for the different enterprise companies are different. Entity: Geo_Map_Points

## Owner Tables Hierarchy

* [Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Map_Point_Id](#map_point_id)|`uniqueidentifier` `PK`||
|[Map_Point_Name](#map_point_name)|`nvarchar(128)` `ML`|Map point short name (Multilanguage)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for within the name of the map point has meaning|
|[Row_Version](#row_version)|`timestamp` ||
|[Latitude](#latitude)|`decimal(10, 7)` |Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90].|
|[Longitude](#longitude)|`decimal(10, 7)` |Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180].|
|[Address](#address)|`nvarchar(128)` |The descriptive physical address, related to this map point.|

## Columns

### Map_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Map_Point_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Latitude

| Property | Value |
| - | - |
|Type|decimal(10, 7)|

### Longitude

| Property | Value |
| - | - |
|Type|decimal(10, 7)|

### Address

| Property | Value |
| - | - |
|Type|nvarchar(128)|


