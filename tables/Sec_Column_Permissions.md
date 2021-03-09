# Table Sec_Column_Permissions

User permissions for accessing the system data columns. Entity: Sec_Column_Permissions

## Summary

| Name | Type | Description |
| - | - | --- |
|[Column_Permission_Id](#column_permission_id)|`uniqueidentifier` `PK`||
|[Table_Name](#table_name)|`nvarchar(128)` |The table in which is the secured column.|
|[Column_Name](#column_name)|`nvarchar(128)` |The name of the secured column.|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` Readonly|The required access key for accessing the column.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Column_Permission_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Table_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Column_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


