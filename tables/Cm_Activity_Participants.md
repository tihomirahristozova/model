# Table Cm_Activity_Participants

Contains the additional participants in the activities. These are the participating users, besides the user to which the activitiy is assigned. Entity: Cm_Activity_Participants

## Owner Tables Hierarchy

* [Cm_Activities](Cm_Activities.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Activity_Participant_Id](#activity_participant_id)|`uniqueidentifier` `PK`||
|[Activity_Id](#activity_id)|`uniqueidentifier` ||
|[Participant_Person_Id](#participant_person_id)|`uniqueidentifier` |The person, participating in an activity|
|[Work_Load_Percent](#work_load_percent)|`decimal(3, 2)` |The planned work load of the participant for this activity.|
|[Notes](#notes)|`nvarchar(255)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Activity_Participant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

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
|Type|nvarchar(255)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


