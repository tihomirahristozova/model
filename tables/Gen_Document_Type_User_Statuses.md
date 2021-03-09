# Table Gen_Document_Type_User_Statuses

User-defined document statuses. Entity: Gen_Document_Type_User_Statuses

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Status_Id](#user_status_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type, to which this user status is bound|
|[State](#state)|`smallint` Allowed: `10`, `20`, `30`, `40`, `50`|The system state to which this user status is bound|
|[User_Status_Name](#user_status_name)|`nvarchar(128)` |Multi-language name of the user status|
|[Display_Order](#display_order)|`int` |Consecutive display order of the status, with regard to other statuses within the same document type|
|[Active](#active)|`bit` |Is the user status active for applying to documents|
|[Instructions](#instructions)|`nvarchar(2147483647)` |Instructions what should be done when this user status is active (Rich Text)|
|[Is_Exit_Status](#is_exit_status)|`bit` |1 when the status allows going to the next system status, 0 otherwise. For example for system status Firm Planned, only user status Approved might allow going to Released|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### State

| Property | Value |
| - | - |
|Type|smallint|

### User_Status_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Display_Order

| Property | Value |
| - | - |
|Type|int|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Instructions

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Is_Exit_Status

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


