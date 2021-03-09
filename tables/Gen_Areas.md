# Table Gen_Areas

Areas are user-defined division of the sales territories. Entity: Gen_Areas

## Summary

| Name | Type | Description |
| - | - | --- |
|[Area_Id](#area_id)|`uniqueidentifier` `PK`||
|[Area_Name](#area_name)|`nvarchar(254)` `ML`||
|[Area_Code](#area_code)|`nvarchar(16)` ||
|[Parent_Area_Id](#parent_area_id)|`uniqueidentifier` |Parent area in the hierarchy.|
|[Full_Path](#full_path)|`nvarchar(254)` Readonly|Full path to the area, starting with '/' and containing the area codes of all parent areas using '/' as separator and terminator. For example root area with code 'BG' would have full path = '/BG/'|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Area_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Area_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Parent_Area_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


