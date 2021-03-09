# Query Bpm_Process_Instances_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Instance_Id](#process_instance_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process on which this instance is based.|
|[Subject](#subject)|`nvarchar` |The multilanguage subject (or title) of this process instance.|
|[State](#state)|`int` Allowed: `0`, `10`, `20`, `60`, Readonly|Instance state. 0=Created; 60=Completed.|
|[Creation_Time](#creation_time)|`datetime` Readonly|The date and time, when the process instance was created.|
|[Start_Time](#start_time)|`datetime` Readonly|The date and time, when the process instance was started.|
|[Finish_Time](#finish_time)|`datetime` Readonly|The date and time, when the process instance has finished its execution. NULL when the instance has not yet finished execution.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Instance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Subject

| Property | Value |
| - | - |
|Type|nvarchar|

### State

| Property | Value |
| - | - |
|Type|int|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Finish_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


