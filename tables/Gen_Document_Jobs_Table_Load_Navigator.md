# Query Gen_Document_Jobs_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Job_Id](#document_job_id)|`uniqueidentifier` `PK`||
|[Job_Id](#job_id)|`uniqueidentifier` |The id of the general job.|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The type of the document, whose state will be changed.|
|[Filter_Xml](#filter_xml)|`nvarchar` |Specifies the documents, whose state will be changed.|
|[New_State](#new_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`, `5`|Specifies the state, which should be set to the documents, matching the filter.|
|[New_User_Status_Id](#new_user_status_id)|`uniqueidentifier` |Specifies the user status, which should be set to the documents, matching the filter. The user statuses are defined for the selected document type.|
|[Job_Type](#job_type)|`nvarchar` Allowed: `DOC`, `POS`, `DNT`, `DPI`|The system type of the job. DOC=Document Change State, POS=Run Postponed Events, DNT=Delete Old Notifications.|
|[Job_Name](#job_name)|`nvarchar` |The name of the job.|
|[Is_Active](#is_active)|`bit` |Specifies whether the job is active and ready for running.|
|[Notes](#notes)|`nvarchar` ||
|[Run_On_Idle](#run_on_idle)|`bit` |Specifies whether to automatically run the job when the server is idle.|

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
|Type|nvarchar|

### New_State

| Property | Value |
| - | - |
|Type|smallint|

### New_User_Status_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Job_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Job_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Run_On_Idle

| Property | Value |
| - | - |
|Type|bit|


