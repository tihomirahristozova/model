# Table Prj_Project_Task_Dependancies

Represents dependancy between project tasks. Entity: Prj_Project_Task_Dependancies

## Owner Tables Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Dependancy_Id](#project_task_dependancy_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The task which depends on another task|
|[Depends_On_Task_Id](#depends_on_task_id)|`uniqueidentifier` |The task on which Project_Task depends|
|[Dependancy_Type](#dependancy_type)|`nvarchar(2)` Allowed: `FS`, `SS`, `FF`, `SF`, `SY`|FS=Finish-to-Start;SS=Start-to-Start;FF=Finish-to-Finish;SF=Start-to-Finish;SY=Sync (all types in the same time)|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Task_Dependancy_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Depends_On_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dependancy_Type

| Property | Value |
| - | - |
|Type|nvarchar(2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


