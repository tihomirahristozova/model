# Table Prj_Project_Tasks

Represents one task of a project. Entity: Prj_Project_Tasks

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` |The project, to which this task belongs.|
|[Project_Work_Element_Id](#project_work_element_id)|`uniqueidentifier` |The work element under which the task is filed.|
|[Task_Name](#task_name)|`nvarchar(254)` |The short name of the task. It is best practice to contain the target of the task.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource, which is required for the task. NULL means - do not plan any resource|
|[Start_Date_Time](#start_date_time)|`datetime` |The date and time when the task is planned to start.|
|[Finish_Date_Time](#finish_date_time)|`datetime` |The date and time when the task is planned to finish.|
|[Work_Type_Id](#work_type_id)|`uniqueidentifier` |Type of work to be done. NULL means that type of work is undetermined yet.|
|[Planned_Duration_Hours](#planned_duration_hours)|`decimal(8, 2)` |Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time.|
|[Budget_Labor_Amount](#budget_labor_amount)|`decimal(12, 2)` |Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. NULL means that budgeting for the item is not calculated|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |The responsible party. Usually a person and usually one of the project participants. NULL means that responsible is not yet determined|
|[Activity_Id](#activity_id)|`uniqueidentifier` |The Id of the Cm_Activity created for this task. NULL means that activity is still not created|
|[Project_Task_No](#project_task_no)|`int` |Consecutive task number, unique within the project.|
|[Task_Type_Id](#task_type_id)|`uniqueidentifier` |The type of the task. Determines the work type of the tasks, default billing rules, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Task_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Finish_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Work_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Duration_Hours

| Property | Value |
| - | - |
|Type|decimal(8, 2)|

### Budget_Labor_Amount

| Property | Value |
| - | - |
|Type|decimal(12, 2)|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_No

| Property | Value |
| - | - |
|Type|int|

### Task_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


