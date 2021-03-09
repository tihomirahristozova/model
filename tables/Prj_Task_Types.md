# Table Prj_Task_Types

Represents the different types of tasks, which can be included in the projects. Entity: Prj_Task_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Task_Type_Id](#task_type_id)|`uniqueidentifier` `PK`||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` |When not NULL, specifies that this task type can be used only for projects of the specified type.|
|[Task_Type_Name](#task_type_name)|`nvarchar(2147483647)` `ML`|The multilanguage task type name.|
|[Icon](#icon)|`varbinary` |Icon representing the task type. Preferrably 32x32 pixels.|
|[Description](#description)|`nvarchar(2147483647)` `ML`|Multilanguage description of the task type.|
|[Display_Order](#display_order)|`int` |Display order position of the task. Lowest numbers are shown first (on top).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Task_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Task_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Icon

| Property | Value |
| - | - |
|Type|varbinary|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Display_Order

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


