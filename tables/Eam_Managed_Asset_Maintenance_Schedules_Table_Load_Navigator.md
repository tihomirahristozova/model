# Query Eam_Managed_Asset_Maintenance_Schedules_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Managed_Asset_Notes](#managed_asset_notes)|`nvarchar` ||
|[Managed_Asset_Group_Id](#managed_asset_group_id)|`uniqueidentifier` |The organizational group of the asset. Used for organizational purposes only.|
|[Managed_Asset_Type_Id](#managed_asset_type_id)|`uniqueidentifier` |The type of the asset. Determines the tracked parameters for the asset, the applicable maintenance types, etc.|
|[Managed_Asset_Name](#managed_asset_name)|`nvarchar` `ML`|Name of the managed asset (multi-language).|
|[Managed_Asset_Code](#managed_asset_code)|`nvarchar` |Unique code of the managed asset. The code is unique among all managed assets in the same enterprise company.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.|
|[Description](#description)|`nvarchar` `ML`|Detailed description of the maintenance (multilanguage).|
|[Maintenance_Type_Name](#maintenance_type_name)|`nvarchar` `ML`|Multilanguage name of the maintenance type.|
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` |The group, to which this maintenance type belongs.|
|[Maintenance_Type_Code](#maintenance_type_code)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Parameter_Change_Delta](#parameter_change_delta)|`int` |The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. NULL means, that the maintenances are not planned, based on parameter change.|
|[Schedule_Days](#schedule_days)|`int` |Number of days between planned maintenances. NULL means that the schedule is not planned based on days.|
|[Schedule_Months](#schedule_months)|`int` |Number of months between planned maintenances. NULL means that the schedule is not planned based on months.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |What type of maintenance is scheduled.|
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The managed asset for which the maintenance schedule applies.|
|[Registration_Number](#registration_number)|`nvarchar` |Registration number of the asset with the national registration authorities. NULL means the registation number is unknown or N/A.|
|[Managed_Asset_Maintenance_Schedule_Id](#managed_asset_maintenance_schedule_id)|`uniqueidentifier` `PK`||

## Columns

### Managed_Asset_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Managed_Asset_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Managed_Asset_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Parameter_Change

| Property | Value |
| - | - |
|Type|int|

### Tracked_Parameter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Schedule_Days

| Property | Value |
| - | - |
|Type|int|

### Default_Schedule_Months

| Property | Value |
| - | - |
|Type|int|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Maintenance_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Maintenance_Type_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Parameter_Change_Delta

| Property | Value |
| - | - |
|Type|int|

### Schedule_Days

| Property | Value |
| - | - |
|Type|int|

### Schedule_Months

| Property | Value |
| - | - |
|Type|int|

### Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Managed_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Registration_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Managed_Asset_Maintenance_Schedule_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


