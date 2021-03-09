# Query Gen_Folders_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Folder_Id](#folder_id)|`uniqueidentifier` `PK`||
|[Parent_Folder_Id](#parent_folder_id)|`uniqueidentifier` |Parent folder. NULL if this is root folder.|
|[Folder_Name](#folder_name)|`nvarchar` |Name of the folder. Unique within its parent folder.|
|[Notes](#notes)|`nvarchar` ||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |The access key, required to unlock the folder contents. NULL means the folder is unprotected and accessible to all internal users.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Folder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Folder_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Folder_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


