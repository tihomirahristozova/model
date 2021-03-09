# Table Prj_Project_Participants

Represents participant in a project, with a specific role. The same participant can participate multiple times in different roles. Entity: Prj_Project_Participants

## Owner Tables Hierarchy

* [Prj_Projects](Prj_Projects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Participant_Id](#project_participant_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` |The project in which the participant will participate|
|[Participant_Party_Id](#participant_party_id)|`uniqueidentifier` |The party Id of the participant|
|[Project_Type_Role_Id](#project_type_role_id)|`uniqueidentifier` |The role which the participant will play in the project. NULL means that the role is undefined|
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Participant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Participant_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


