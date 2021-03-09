# Table Gen_Geo_Points

Geographical (geo) points are used as points of interest on the map. They are used for routing and other purposes. The points of interest for the different enterprise companies are different. Entity: Gen_Geo_Points

## Summary

| Name | Type | Description |
| - | - | --- |
|[Geo_Point_Id](#geo_point_id)|`uniqueidentifier` `PK`||
|[Geo_Point_Name](#geo_point_name)|`nvarchar(128)` `ML`|Geo point short name (Multilanguage)|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the name of the geo point has meaning. Null for geo points not related to specific enterprise company.|
|[Latitude](#latitude)|`decimal(10, 7)` |Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90].|
|[Longitude](#longitude)|`decimal(10, 7)` |Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180].|
|[Address](#address)|`nvarchar(128)` |The descriptive physical address, related to this geo point.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Geo_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Geo_Point_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


