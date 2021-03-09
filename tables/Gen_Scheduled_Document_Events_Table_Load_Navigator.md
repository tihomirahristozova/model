# Query Gen_Scheduled_Document_Events_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Scheduled_Document_Event_Id](#scheduled_document_event_id)|`uniqueidentifier` `PK`||
|[Source_Document_Id](#source_document_id)|`uniqueidentifier` Readonly||
|[Document_Event](#document_event)|`nvarchar` Readonly||
|[Document_Id](#document_id)|`uniqueidentifier` Readonly||
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly||
|[Processed](#processed)|`bit` Readonly||
|[Last_Process_Time](#last_process_time)|`datetime` Readonly||
|[Last_Process_Status](#last_process_status)|`nvarchar` Readonly||
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Cancelled](#cancelled)|`bit` ||
|[Document_Date](#document_date)|`date` ||

## Columns

### Scheduled_Document_Event_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Source_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Event

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### State

| Property | Value |
| - | - |
|Type|smallint|

### Processed

| Property | Value |
| - | - |
|Type|bit|

### Last_Process_Time

| Property | Value |
| - | - |
|Type|datetime|

### Last_Process_Status

| Property | Value |
| - | - |
|Type|nvarchar|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Cancelled

| Property | Value |
| - | - |
|Type|bit|

### Document_Date

| Property | Value |
| - | - |
|Type|date|


