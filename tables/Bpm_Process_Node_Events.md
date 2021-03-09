# Table Bpm_Process_Node_Events

Abstract root of all process node events. Currently - not used. Entity: Bpm_Process_Node_Events

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Node_Event_Id](#process_node_event_id)|`uniqueidentifier` `PK`||
|[Process_Node_Id](#process_node_id)|`uniqueidentifier` |The node of this node event.|
|[Event_Type](#event_type)|`nvarchar(1)` |Event type. S=Start, T=Intermediate Throw, C=Intermediate Catch, B=Boundary, E=End.|
|[Is_Message](#is_message)|`bit` |True if this is message event.|
|[Is_Timer](#is_timer)|`bit` |True if this is timer event.|
|[Is_Signal](#is_signal)|`bit` |True if this is signal event.|
|[Is_Escalation](#is_escalation)|`bit` |True if this is escalation event.|
|[Is_Error](#is_error)|`bit` |True if this is error event.|
|[Is_Cancel](#is_cancel)|`bit` |True if this is cancel event.|
|[Is_Compensation](#is_compensation)|`bit` |True if this is compensation event.|
|[Event_Key](#event_key)|`nvarchar(128)` |The unique event key, which is thrown or caught.|
|[Boundary_Of_Process_Node_Id](#boundary_of_process_node_id)|`uniqueidentifier` |When the event is boundary, contains the node to which the event is bound. Otherwise contains NULL.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Node_Event_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Event_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Is_Message

| Property | Value |
| - | - |
|Type|bit|

### Is_Timer

| Property | Value |
| - | - |
|Type|bit|

### Is_Signal

| Property | Value |
| - | - |
|Type|bit|

### Is_Escalation

| Property | Value |
| - | - |
|Type|bit|

### Is_Error

| Property | Value |
| - | - |
|Type|bit|

### Is_Cancel

| Property | Value |
| - | - |
|Type|bit|

### Is_Compensation

| Property | Value |
| - | - |
|Type|bit|

### Event_Key

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Boundary_Of_Process_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


