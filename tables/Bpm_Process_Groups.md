# Table Bpm_Process_Groups

Represents a node in the hierarchy of process groups. Entity: Bpm_Process_Groups

## Summary

| Name | Type | Description |
| - | - | --- |
|[Process_Group_Id](#process_group_id)|`uniqueidentifier` `PK`||
|[Parent_Process_Group_Id](#parent_process_group_id)|`uniqueidentifier` |Parent process group in the hierarchy. NULL means this is a root group.|
|[Process_Group_Code](#process_group_code)|`nvarchar(5)` |Group code, unique within the parent group.|
|[Process_Group_Name](#process_group_name)|`nvarchar(254)` `ML`|Multilanguage process group name|
|[Notes](#notes)|`nvarchar(2147483647)` ||
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
|Type|nvarchar(5)|

### Process_Group_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


