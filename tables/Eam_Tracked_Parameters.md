# Table Eam_Tracked_Parameters

Parameters of assets, tracked for maintenance reasons, like car mileage, aircraft cycles, etc. Entity: Eam_Tracked_Parameters (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` `PK`||
|[Tracked_Parameter_Code](#tracked_parameter_code)|`nvarchar(16)` |Unique code of the asset parameter.|
|[Tracked_Parameter_Name](#tracked_parameter_name)|`nvarchar(254)` `ML`|Multilanguage name of the asset parameter.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the parameter is active for choosing in drop downs.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Tracked_Parameter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tracked_Parameter_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Tracked_Parameter_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


