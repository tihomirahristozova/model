# Query Bpm_Processes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Id](#process_id)|`uniqueidentifier` `PK`||
|[Process_Code](#process_code)|`nvarchar` |Unique process code.|
|[Process_Name](#process_name)|`nvarchar` ||
|[Process_Group_Id](#process_group_id)|`uniqueidentifier` |The process group, to which this process belongs.|
|[Locality](#locality)|`nvarchar` Allowed: `P`, `L`, `C`, `I`|Process execution locality. Represents where the execution takes place and influences the selection of possible executors. For example, when L, the execution is private to the location, where the process originated. P=Same as parent; L=Location; C=Company; I=Intra-company.|
|[Is_Executable](#is_executable)|`bit` |Specifies whether the process is executable. In order to be executable, a process must contain enough execution details. Note, that some processes are only for documentation purposes and are not intended to be executed.|
|[Is_Published](#is_published)|`bit` |Specifies whether the process is currently published for new instances.|
|[Description](#description)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Process_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Process_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Locality

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


