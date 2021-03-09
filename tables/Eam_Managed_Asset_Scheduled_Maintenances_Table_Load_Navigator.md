# Query Eam_Managed_Asset_Scheduled_Maintenances_Table_Load_Navigator


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
|[Is_Dismissed](#is_dismissed)|`bit` |Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action.|
|[Tracked_Parameter_Value](#tracked_parameter_value)|`int` |The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. NULL means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.|
|[Date](#date)|`date` |The date, when the maintenance is planned. NULL means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met.|
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` |The type of maintenance, which will be performed.|
|[Managed_Asset_Id](#managed_asset_id)|`uniqueidentifier` |The asset, which will be maintained.|
|[Registration_Number](#registration_number)|`nvarchar` |Registration number of the asset with the national registration authorities. NULL means the registation number is unknown or N/A.|
|[Managed_Asset_Scheduled_Maintenance_Id](#managed_asset_scheduled_maintenance_id)|`uniqueidentifier` `PK`||

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

### Is_Dismissed

| Property | Value |
| - | - |
|Type|bit|

### Tracked_Parameter_Value

| Property | Value |
| - | - |
|Type|int|

### Date

| Property | Value |
| - | - |
|Type|date|

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

### Managed_Asset_Scheduled_Maintenance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


