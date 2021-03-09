# Table Eam_Managed_Asset_Maintenance_Schedules

Contains the maintenance schedules for the managed assets. Entity: Eam_Managed_Asset_Maintenance_Schedules (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Eam_Managed_Assets](Eam_Managed_Assets.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Maintenance_Schedule_Id](#managed_asset_maintenance_schedule_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The managed asset for which the maintenance schedule applies.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |What type of maintenance is scheduled.|
|[Schedule_Months](#schedule_months)|`int` |Number of months between planned maintenances. NULL means that the schedule is not planned based on months.|
|[Schedule_Days](#schedule_days)|`int` |Number of days between planned maintenances. NULL means that the schedule is not planned based on days.|
|[Parameter_Change_Delta](#parameter_change_delta)|`int` |The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. NULL means, that the maintenances are not planned, based on parameter change.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Managed_Asset_Maintenance_Schedule_Id

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

### Schedule_Months

| Property | Value |
| - | - |
|Type|int|

### Schedule_Days

| Property | Value |
| - | - |
|Type|int|

### Parameter_Change_Delta

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


