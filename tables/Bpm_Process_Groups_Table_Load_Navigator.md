# Query Bpm_Process_Groups_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Group_Id](#process_group_id)|`uniqueidentifier` `PK`||
|[Parent_Process_Group_Id](#parent_process_group_id)|`uniqueidentifier` |Parent process group in the hierarchy. NULL means this is a root group.|
|[Process_Group_Code](#process_group_code)|`nvarchar` |Group code, unique within the parent group.|
|[Process_Group_Name](#process_group_name)|`nvarchar` `ML`|Multilanguage process group name|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Process_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Process_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Process_Group_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Process_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


