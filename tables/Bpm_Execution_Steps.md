# Table Bpm_Execution_Steps

Contains both historical and active steps in the execution of the business processes. Entity: Bpm_Execution_Steps

## Summary

| Name | Type | Description |
| - | - | --- |
|[Execution_Step_Id](#execution_step_id)|`uniqueidentifier` `PK`||
|[Process_Instance_Id](#process_instance_id)|`uniqueidentifier` |The process instance, which is being executed.|
|[Process_Element_Id](#process_element_id)|`uniqueidentifier` |The process element, which is being executed for the instance.|
|[Execution_State](#execution_state)|`int` |Shows where the execution of the step has reached. 0=Ready; 10=Active; 20=Executing; 30=Completing; 40=Failing; 50=Terminating; 60=Completed; 70=Failed; 80=Terminated.|
|[Start_Time](#start_time)|`datetime` |The date and time when the step execution started.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Execution_Step_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Instance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Execution_State

| Property | Value |
| - | - |
|Type|int|

### Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


