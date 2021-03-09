# Table Wf_Process_Steps


## Owner Tables Hierarchy

* [Wf_Processes](Wf_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Step_Id](#process_step_id)|`uniqueidentifier` `PK`|Unique process step Id|
|[Process_Id](#process_id)|`uniqueidentifier` |The process, to which this step belongs|
|[Step_Code](#step_code)|`nvarchar(6)` |Unique code of the step. Used to sort the steps for display purposes|
|[Step_Type](#step_type)|`nvarchar(3)` |Step type. STU=Start step (by user action); STE=Start step - by email; END=Ending step; ACT=User action; CHO=Choice|
|[Short_Title](#short_title)|`nvarchar(128)` |Very short multilanguage title, displayed on the process diagram. The user text should be 15-20 chars, for each language|
|[Role_Id](#role_id)|`uniqueidentifier` |The role responsible for execution of the step|
|[Instructions](#instructions)|`nvarchar(2147483647)` |Full decription and instructions for the step. Displayed to user when executing the step|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Step_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Step_Code

| Property | Value |
| - | - |
|Type|nvarchar(6)|

### Step_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Short_Title

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Instructions

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


