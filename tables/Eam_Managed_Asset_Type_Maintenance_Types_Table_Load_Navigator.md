# Query Eam_Managed_Asset_Type_Maintenance_Types_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Type_Maintenance_Type_Id](#managed_asset_type_maintenance_type_id)|`uniqueidentifier` `PK`||
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The asset type for which the allowed maintenance type is defined.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The allowed maintenance type for the asset type.|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in months.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means that there is no default schedule in days.|
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. NULL means, that maintenances are not scheduled based on parameter change.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Managed_Asset_Type_Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Schedule_Months

| Property | Value |
| - | - |
|Type|int|

### Default_Schedule_Days

| Property | Value |
| - | - |
|Type|int|

### Default_Parameter_Change

| Property | Value |
| - | - |
|Type|int|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


