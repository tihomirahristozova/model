# Query Eam_Maintenance_Types_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Maintenance_Type_Id](#maintenance_type_id)|`uniqueidentifier` `PK`||
|[Maintenance_Type_Code](#maintenance_type_code)|`nvarchar` |Unique code of the maintenance type.|
|[Maintenance_Type_Group_Id](#maintenance_type_group_id)|`uniqueidentifier` |The group, to which this maintenance type belongs.|
|[Maintenance_Type_Name](#maintenance_type_name)|`nvarchar` `ML`|Multilanguage name of the maintenance type.|
|[Description](#description)|`nvarchar` `ML`|Detailed description of the maintenance (multilanguage).|
|[Default_Schedule_Months](#default_schedule_months)|`int` |Specifies the maximum number of months between two maintenances. NULL means that there is no default schedule in months.|
|[Default_Schedule_Days](#default_schedule_days)|`int` |Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). NULL means that there is no default schedule in days.|
|[Tracked_Parameter_Id](#tracked_parameter_id)|`uniqueidentifier` |Specifies the parameter, on which the next scheduled maintenance will be based. NULL means that there is no default schedule, based on parameter.|
|[Default_Parameter_Change](#default_parameter_change)|`int` |Default positive change of the tracked parameter between two maintenances. NULL means, that maintenances are not scheduled based on parameter change.|
|[Maintenance_Type_Group_Code](#maintenance_type_group_code)|`nvarchar` |Unique code of the group.|
|[Parent_Maintenance_Type_Group_Id](#parent_maintenance_type_group_id)|`uniqueidentifier` |Parent group. NULL denotes a root group.|
|[Maintenance_Type_Group_Name](#maintenance_type_group_name)|`nvarchar` `ML`|Multilanguage name of the group.|
|[Notes](#notes)|`nvarchar` ||

## Columns

### Maintenance_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Maintenance_Type_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Maintenance_Type_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Maintenance_Type_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Maintenance_Type_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|


