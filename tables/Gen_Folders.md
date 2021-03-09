# Table Gen_Folders

Folders are the base for the file storage within the system. Each folder is a data object, with the primary idea of containing files. Entity: Gen_Folders (Introduced in version 21.1.1.8)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Folder_Id](#folder_id)|`uniqueidentifier` `PK`||
|[Parent_Folder_Id](#parent_folder_id)|`uniqueidentifier` |Parent folder. NULL if this is root folder.|
|[Folder_Name](#folder_name)|`nvarchar(128)` |Name of the folder. Unique within its parent folder.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
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
|Type|nvarchar(128)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


