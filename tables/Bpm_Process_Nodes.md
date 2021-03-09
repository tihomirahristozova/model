# Table Bpm_Process_Nodes

Contains the flow Nodes of the process model. Entity: Bpm_Process_Nodes

## Owner Tables Hierarchy

* [Bpm_Processes](Bpm_Processes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Node_Id](#process_node_id)|`uniqueidentifier` `PK`||
|[Process_Id](#process_id)|`uniqueidentifier` |The process, to which this Node belongs.|
|[Process_Lane_Id](#process_lane_id)|`uniqueidentifier` |The process lane to which this Node belongs.|
|[Process_Node_Code](#process_node_code)|`nvarchar(16)` |Node code, unique within the process. Used as ID for XML serialization purposes.|
|[Process_Node_Name](#process_node_name)|`nvarchar(512)` `ML`|Multilanguage process name.|
|[Node_Type](#node_type)|`nvarchar(1)` Allowed: `A`, `E`, `G`, `C`|Type of the node. A=Text Annotation; E=Event; G=Gateway; T=Task; P=Sub-Process.|
|[Instructions_Html](#instructions_html)|`nvarchar(2147483647)` |Detailed instructions to the executor in HTML format.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Node_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Lane_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Node_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Process_Node_Name

| Property | Value |
| - | - |
|Type|nvarchar(512)|

### Node_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Instructions_Html

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


