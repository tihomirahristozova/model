# Query Prj_Project_Task_Participants_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Participant_Id](#project_task_participant_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the participant is planned.|
|[Participant_Person_Id](#participant_person_id)|`uniqueidentifier` ||
|[Work_Load_Percent](#work_load_percent)|`decimal(0, 0)` |The planned work load (in percents) of the participant for this task.|
|[Notes](#notes)|`nvarchar` ||
|[Notify_On_Status_Change](#notify_on_status_change)|`bit` |Specifies whether the participant should be notified on task status changes.|
|[Project_Id](#project_id)|`uniqueidentifier` |The project, to which this task belongs.|
|[Project_Work_Element_Id](#project_work_element_id)|`uniqueidentifier` |The work element under which the task is filed.|
|[Task_Name](#task_name)|`nvarchar` |The short name of the task. It is best practice to contain the target of the task.|
|[Start_Date_Time](#start_date_time)|`datetime` |The date and time when the task is planned to start.|
|[Finish_Date_Time](#finish_date_time)|`datetime` |The date and time when the task is planned to finish.|
|[Work_Type_Id](#work_type_id)|`uniqueidentifier` |Type of work to be done. NULL means that type of work is undetermined yet.|
|[Planned_Duration_Hours](#planned_duration_hours)|`decimal(0, 0)` |Planned duration of the task in hours. The hours are allocated in the time interval between Start Date Time and Finish Date Time.|
|[Budget_Labor_Amount](#budget_labor_amount)|`decimal(0, 0)` |Budgeted amount for the labor for the task in the currency of the project. The material is calculated separately. NULL means that budgeting for the item is not calculated|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |The responsible party. Usually a person and usually one of the project participants. NULL means that responsible is not yet determined|
|[Activity_Id](#activity_id)|`uniqueidentifier` |The Id of the Cm_Activity created for this task. NULL means that activity is still not created|
|[Project_Task_No](#project_task_no)|`int` |Consecutive task number, unique within the project.|
|[Task_Type_Id](#task_type_id)|`uniqueidentifier` |The type of the task. Determines the work type of the tasks, default billing rules, etc.|

## Columns

### Project_Task_Participant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Participant_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Load_Percent

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Notify_On_Status_Change

| Property | Value |
| - | - |
|Type|bit|

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
|Type|nvarchar|

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
|Type|decimal(0, 0)|

### Budget_Labor_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

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


