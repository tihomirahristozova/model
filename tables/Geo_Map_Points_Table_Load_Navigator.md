# Query Geo_Map_Points_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Map_Point_Id](#map_point_id)|`uniqueidentifier` `PK`||
|[Map_Point_Name](#map_point_name)|`nvarchar` `ML`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Latitude](#latitude)|`decimal(0, 0)` |Latitude is the vertical angle from equator to the pole of the point. Positive values denote points north of the equator. The value is in the range [-90, 90].|
|[Longitude](#longitude)|`decimal(0, 0)` |Longitude is angle from the prime meridian (in England) in east-west direction. Positive values denote east and negative - west. The value is in the range [-180, 180].|
|[Address](#address)|`nvarchar` |The descriptive physical address, related to this map point.|

## Columns

### Map_Point_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Map_Point_Name

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|decimal(0, 0)|

### Longitude

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Address

| Property | Value |
| - | - |
|Type|nvarchar|


