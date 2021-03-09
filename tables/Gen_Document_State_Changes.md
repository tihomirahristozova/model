# Table Gen_Document_State_Changes

History of document state changes. Entity: Gen_Document_State_Changes

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_State_Change_Id](#document_state_change_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document which has changed state.|
|[New_State](#new_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`, `5`|The new state after the change.|
|[Update_Time](#update_time)|`datetime` |The time when the change took effect.|
|[Update_User](#update_user)|`nvarchar(64)` |The login name of the user, who made the status change|
|[User_Status_Id](#user_status_id)|`uniqueidentifier` |The new user status after the change.|
|[System_Initiated](#system_initiated)|`bit` Readonly||
|[Row_Version](#row_version)|`timestamp` ||
|[Void](#void)|`bit` |1 if the document is voided with this change|

## Columns

### Document_State_Change_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### New_State

| Property | Value |
| - | - |
|Type|smallint|

### Update_Time

| Property | Value |
| - | - |
|Type|datetime|

### Update_User

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### System_Initiated

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Void

| Property | Value |
| - | - |
|Type|bit|


