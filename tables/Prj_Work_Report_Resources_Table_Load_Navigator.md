# Query Prj_Work_Report_Resources_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Work_Report_Resource_Id](#work_report_resource_id)|`uniqueidentifier` `PK`||
|[Work_Report_Id](#work_report_id)|`uniqueidentifier` ||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the work is reported.|
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource, for which usage is reported.|
|[Resource_Instance_Id](#resource_instance_id)|`uniqueidentifier` |The concrete resource instance used. NULL when no concrete resource was used or there is no data whether concrete resource was used.|
|[Total_Resource_Usage_Hours](#total_resource_usage_hours)|`decimal(18, 2)` |The total number of resource-hours, which are actually consumed. Equals to the duration of the task, multiplied by the average resource usage.|
|[Actual_Start_Time](#actual_start_time)|`datetime` |Optionally, specifies the actual date and time when the resource usage began.|
|[Actual_End_Time](#actual_end_time)|`datetime` |Optionally, specifies the actual date and time when the resource usage ended.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Work_Report_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Report_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Instance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Total_Resource_Usage_Hours

| Property | Value |
| - | - |
|Type|decimal(18, 2)|

### Actual_Start_Time

| Property | Value |
| - | - |
|Type|datetime|

### Actual_End_Time

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


