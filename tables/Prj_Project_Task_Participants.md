# Table Prj_Project_Task_Participants

Contains the participants in the project tasks. Entity: Prj_Project_Task_Participants

## Owner Tables Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Participant_Id](#project_task_participant_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the participant is planned.|
|[Participant_Person_Id](#participant_person_id)|`uniqueidentifier` |The person, who is planned to participate in the project task|
|[Work_Load_Percent](#work_load_percent)|`decimal(3, 2)` |The planned work load (in percents) of the participant for this task.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Notify_On_Status_Change](#notify_on_status_change)|`bit` |Specifies whether the participant should be notified on task status changes.|
|[Row_Version](#row_version)|`timestamp` ||

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
|Type|decimal(3, 2)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notify_On_Status_Change

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


