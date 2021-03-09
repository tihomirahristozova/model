# Table Gen_Document_Jobs

Represents jobs, which change state of documents. Entity: Gen_Document_Jobs (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Sys_Jobs](Sys_Jobs.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Job_Id](#document_job_id)|`uniqueidentifier` `PK`||
|[Job_Id](#job_id)|`uniqueidentifier` |The id of the general job.|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The type of the document, whose state will be changed.|
|[Filter_Xml](#filter_xml)|`nvarchar(2147483647)` |Specifies the documents, whose state will be changed.|
|[New_State](#new_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`, `5`|Specifies the state, which should be set to the documents, matching the filter.|
|[Row_Version](#row_version)|`timestamp` ||
|[New_User_Status_Id](#new_user_status_id)|`uniqueidentifier` |Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type.|

## Columns

### Document_Job_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Job_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Filter_Xml

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### New_State

| Property | Value |
| - | - |
|Type|smallint|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### New_User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


