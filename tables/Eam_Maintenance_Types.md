# Table Eam_Maintenance_Types

Types of maintenances which can be scheduled and performed on the managed assets. Maintenances can be scheduled based on date and tracked parameter change. Entity: Eam_Maintenance_Types (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` `PK`||
|[Maintenance_Type_Code](#maintenance_type_code)|`nvarchar(16)` |Unique code of the maintenance type.|
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` |The group, to which this maintenance type belongs.|
|[Maintenance_Type_Name](#maintenance_type_name)|`nvarchar(254)` `ML`|Multilanguage name of the maintenance type.|
|[Description](#description)|`nvarchar(2147483647)` `ML`|Detailed description of the maintenance (multilanguage).|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.|
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Maintenance_Type_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Default_Schedule_Months

| Property | Value |
| - | - |
|Type|int|

### Default_Schedule_Days

| Property | Value |
| - | - |
|Type|int|

### Tracked_Parameter_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Parameter_Change

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


