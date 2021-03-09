# Query Prj_Project_Participants_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Participant_Id](#project_participant_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` |The project in which the participant will participate|
|[Participant_Party_Id](#participant_party_id)|`uniqueidentifier` |The party Id of the participant|
|[Project_Type_Role_Id](#project_type_role_id)|`uniqueidentifier` |The role which the participant will play in the project. NULL means that the role is undefined|
|[Notes](#notes)|`nvarchar` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Project_Name](#project_name)|`nvarchar` ||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` |The project type defines the basic WBS and default tasks, etc. It is also used as baseline WBS, when combining reports for many projects|
|[Start_Date](#start_date)|`date` |Expected date, when the execution of the tasks will start. NULL means that the start date is still unknown|
|[Finish_Date](#finish_date)|`date` |The drop dead date of the project, e.g. the date when the project should be finished. NULL means that the finish date is unknown.|
|[Project_Manager_Person_Id](#project_manager_person_id)|`uniqueidentifier` |The project manager|
|[Client_Party_Id](#client_party_id)|`uniqueidentifier` |The external or internal client of the project|
|[Project_Status](#project_status)|`tinyint` Allowed: `0`, `10`, `20`, `30`, `40`, `45`, `50`, `55`|Current project status. 0=New, 10=Planned, 30=Started, 40=Resolved(Completed), 45=Resolved(Cancelled), 50=Closed(Completed), 55=Closed(Cancelled)|
|[Budgeting_Currency_Id](#budgeting_currency_id)|`uniqueidentifier` |The currency in which the project budget is calculated|
|[Project_Code](#project_code)|`nvarchar` |Short code for identification of projects.|

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
|Type|nvarchar|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|date|

### Finish_Date

| Property | Value |
| - | - |
|Type|date|

### Project_Manager_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Client_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Status

| Property | Value |
| - | - |
|Type|tinyint|

### Budgeting_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Code

| Property | Value |
| - | - |
|Type|nvarchar|


