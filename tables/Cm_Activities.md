# Table Cm_Activities

Generic activity. Provides task management functionality. Activity can be one of Task, Communication or Meeting. Entity: Cm_Activities

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[System_Type](#system_type)|`nvarchar(1)` Allowed: `C`, `M`, `T`|T=Task; C=Communication; M=Meeting|
|[Subject](#subject)|`nvarchar(254)` |Task primary subject (required)|
|[Notes](#notes)|`nvarchar(254)` ||
|[Target_Party_Id](#target_party_id)|`uniqueidentifier` |External participant or target of the task|
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` |Who is responsible for executing the task. Initially this is the owner of the task|
|[Owner_Party_Id](#owner_party_id)|`uniqueidentifier` |The party that owns the task. Initially this is the party that has created the task|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|Priority on the scale from 1 (least important) to 5 (very important)|
|[Private](#private)|`bit` |1 if the task is visible only to its owner; 0 if this is publicly visible task|
|[Start_Time](#start_time)|`datetime` |Currently planned starting time of the task|
|[End_Time](#end_time)|`datetime` |Currently planned ending time of the task|
|[Reminder_Time](#reminder_time)|`datetime` |When to snooze to the owner to remind him for the task. This default reminder is copied to and managed by the Reminders entity.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the work is performed. NULL when the activity is not related to a project task.|
|[Planned_Duration_Minutes](#planned_duration_minutes)|`int` |Total planned duration of the activity, regardless of the current execution status|
|[Activity_Id](#activity_id)|`uniqueidentifier` `PK`||
|[Deadline_Time](#deadline_time)|`datetime` |The deadline for the task. NULL if there is no deadline|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Document_Id](#document_id)|`uniqueidentifier` |The task's document (for entry date, task type, status)|
|[Contact_Person_Id](#contact_person_id)|`uniqueidentifier` |The contact person, from the side of the Target Party.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### System_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Subject

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Target_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Owner_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|

### Private

| Property | Value |
| - | - |
|Type|bit|

### Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Reminder_Time

| Property | Value |
| - | - |
|Type|datetime|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Duration_Minutes

| Property | Value |
| - | - |
|Type|int|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Deadline_Time

| Property | Value |
| - | - |
|Type|datetime|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contact_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


