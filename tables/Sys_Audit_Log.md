# Table Sys_Audit_Log


## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Id](#object_id)|`uniqueidentifier` `PK`|The Id of the affected object|
|[Operation_System_User](#operation_system_user)|`nvarchar(256)` `PK`|Not used.|
|[Operation_Time](#operation_time)|`datetime` `PK`|Not used.|
|[Operation_Type](#operation_type)|`nvarchar(10)` `PK`|The type of operation - I=INSERT, D=DELETE, U=UPDATE|
|[Old_Values_XML](#old_values_xml)|`nvarchar(2147483647)` |Values of the document columns (without BLOBs) before the operation |
|[New_Values_XML](#new_values_xml)|`nvarchar(2147483647)` |The new values of the columns|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_System_User

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Operation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Operation_Type

| Property | Value |
| - | - |
|Type|nvarchar(10)|

### Old_Values_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### New_Values_XML

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


