# Table Prj_Project_Risk_Discussion

Contains discussions on project risks. Entity: Prj_Project_Risk_Discussion

## Owner Tables Hierarchy

* [Prj_Project_Risks](Prj_Project_Risks.md)
* [Prj_Projects](Prj_Projects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Risk_Message_Id](#project_risk_message_id)|`uniqueidentifier` `PK`||
|[Project_Risk_Id](#project_risk_id)|`uniqueidentifier` ||
|[Contributed_By_User_Id](#contributed_by_user_id)|`uniqueidentifier` Readonly|The user, who contributed (wrote) the message.|
|[Contribution_Time](#contribution_time)|`datetime` Readonly|The time, when the message was contributed.|
|[Message](#message)|`nvarchar(2147483647)` |The contents of the message.|
|[Last_Edit_Time](#last_edit_time)|`datetime` Readonly|Contains the last edit time of the message. NULL if the message was never edited|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Risk_Message_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Risk_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contributed_By_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contribution_Time

| Property | Value |
| - | - |
|Type|datetime|

### Message

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Last_Edit_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


