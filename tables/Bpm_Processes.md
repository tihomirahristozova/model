# Table Bpm_Processes

Represents one business process version. All process model elements and execution instances are bound to specfic process version. Entity: Bpm_Processes

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Id](#process_id)|`uniqueidentifier` `PK`||
|[Process_Code](#process_code)|`nvarchar(16)` |Unique process code.|
|[Process_Name](#process_name)|`nvarchar(254)` ||
|[Process_Group_Id](#process_group_id)|`uniqueidentifier` |The process group, to which this process belongs.|
|[Locality](#locality)|`nvarchar(1)` Allowed: `P`, `L`, `C`, `I`|Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company.|
|[Is_Executable](#is_executable)|`bit` |Specifies whether the process is executable. In order to be executable, a process must contain enough execution details. Note, that some processes are only for documentation purposes and are not intended to be executed.|
|[Is_Published](#is_published)|`bit` |Specifies whether the process is currently published for new instances.|
|[Description](#description)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Process_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Process_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Locality

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Is_Executable

| Property | Value |
| - | - |
|Type|bit|

### Is_Published

| Property | Value |
| - | - |
|Type|bit|

### Description

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


