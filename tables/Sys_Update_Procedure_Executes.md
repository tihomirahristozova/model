# Table Sys_Update_Procedure_Executes

Contains data about the execution of Upgrade Procedures. Contains status messages and ensures that each procedure is executed only once. Entity: Sys_Update_Procedure_Executes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Update_Procedure_Execute_Id](#update_procedure_execute_id)|`uniqueidentifier` `PK`||
|[Update_Procedure](#update_procedure)|`nvarchar(128)` |The system name of the executed update procedure.|
|[Execute_Time](#execute_time)|`datetime` |The time, when the update procedure was executed.|
|[Successful](#successful)|`bit` |True when the execution was successfull.|
|[Result_Message](#result_message)|`nvarchar(1024)` |Error or success message|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Update_Procedure_Execute_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Update_Procedure

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Execute_Time

| Property | Value |
| - | - |
|Type|datetime|

### Successful

| Property | Value |
| - | - |
|Type|bit|

### Result_Message

| Property | Value |
| - | - |
|Type|nvarchar(1024)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


