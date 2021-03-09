# Table Sys_Jobs

The jobs, which are configured in the system. Entity: Sys_Jobs (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Job_Id](#job_id)|`uniqueidentifier` `PK`||
|[Job_Type](#job_type)|`nvarchar(3)` Allowed: `DOC`, `POS`, `DNT`, `DPI`|The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications.|
|[Job_Name](#job_name)|`nvarchar(254)` |The name of the job.|
|[Is_Active](#is_active)|`bit` |Specifies whether the job is active and ready for running.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Run_On_Idle](#run_on_idle)|`bit` |Specifies whether to automatically run the job when the server is idle.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Job_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Job_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Job_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Run_On_Idle

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


