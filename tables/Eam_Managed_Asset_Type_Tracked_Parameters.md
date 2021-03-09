# Table Eam_Managed_Asset_Type_Tracked_Parameters

Defines the parameters, which are tracked for the assets of the different types. Entity: Eam_Managed_Asset_Type_Tracked_Parameters (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Eam_Managed_Asset_Types](Eam_Managed_Asset_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Type_Tracked_Parameter_Id](#managed_asset_type_tracked_parameter_id)|`uniqueidentifier` `PK`|Defines the parameters, which are tracked for the assets of the different types.|
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The asset type for which the tracked parameter is defined.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |The parameter, which will be tracked for assets of the specified type.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Type_Tracked_Parameter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Tracked_Parameter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


