# Table Eam_Managed_Asset_Scheduled_Maintenances

Contains the scheduled maintenances for the managed assets. Each maintenance can be planned based on date, parameter value or both. Past maintenance plans are kept only for reference and can be deleted at any time. Entity: Eam_Managed_Asset_Scheduled_Maintenances (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Scheduled_Maintenance_Id](#managed_asset_scheduled_maintenance_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The asset, which will be maintained.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The type of maintenance, which will be performed.|
|[Date](#date)|`date` |The date, when the maintenance is planned. NULL means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.|
|[Tracked_Parameter_Value](#tracked_parameter_value)|`int` |The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. NULL means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.|
|[Is_Dismissed](#is_dismissed)|`bit` |Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Scheduled_Maintenance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Date

| Property | Value |
| - | - |
|Type|date|

### Tracked_Parameter_Value

| Property | Value |
| - | - |
|Type|int|

### Is_Dismissed

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


