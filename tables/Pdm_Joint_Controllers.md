# Table Pdm_Joint_Controllers

Contains relationship between process and joint controllers. For processes with control role, these are the joint controllers. Otherwise, these are the joint controllers, on behalf of which the enterprise company processes the data. Entity: Pdm_Joint_Controllers (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Pdm_Personal_Data_Processes](Pdm_Personal_Data_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Joint_Controller_Id](#joint_controller_id)|`uniqueidentifier` `PK`||
|[Personal_Data_Process_Id](#personal_data_process_id)|`uniqueidentifier` |The process, which is managed jointly.|
|[Joint_Controller_Party_Id](#joint_controller_party_id)|`uniqueidentifier` |The party, controlling the process.|
|[Notes](#notes)|`nvarchar(2147483647)` |Should usually contain a short description of the role of the joint controller.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Joint_Controller_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Personal_Data_Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Joint_Controller_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


