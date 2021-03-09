# Table Gen_Scheduled_Document_Events

Contains postponed events, which will be executed later. Usually these are large number of recalculation events, resulting from other events. For example, releasing a cost correction, publishes postponed events for all affected documents. Entity: Gen_Scheduled_Document_Events

## Summary

| Name | Type | Description |
| - | - | --- |
|[Scheduled_Document_Event_Id](#scheduled_document_event_id)|`uniqueidentifier` `PK`||
|[Source_Document_Id](#source_document_id)|`uniqueidentifier` Readonly|The document that has caused this event to be scheduled|
|[Document_Event](#document_event)|`nvarchar(254)` Readonly|The type of the document event that is scheduled to be processed|
|[Document_Id](#document_id)|`uniqueidentifier` Readonly|The document for which the event will be processed|
|[State](#state)|`smallint` Allowed: `0`, `5`, `10`, `20`, `30`, `40`, `50`, Readonly|The state of the document for which the event will be processed|
|[Processed](#processed)|`bit` Readonly|Indicates wheather the event is already processed or not|
|[Last_Process_Time](#last_process_time)|`datetime` Readonly|The time of the last attempt to process the event|
|[Last_Process_Status](#last_process_status)|`nvarchar(2147483647)` Readonly|Status/information of the last attemp to process the event. Usually shows the cause in case of failure.|
|[Creation_Time](#creation_time)|`datetime` Readonly||
|[Cancelled](#cancelled)|`bit` |When true, specifies that this document event has been cancelled (either manually or in respect to another event) and will not be executed.|
|[Row_Version](#row_version)|`timestamp` ||

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
|Type|nvarchar(254)|

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
|Type|nvarchar(2147483647)|

### Creation_Time

| Property | Value |
| - | - |
|Type|datetime|

### Cancelled

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


