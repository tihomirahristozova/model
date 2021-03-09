# Query Pos_Roles_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Role_Id](#pos_role_id)|`uniqueidentifier` `PK`||
|[Pos_Role_Code](#pos_role_code)|`nvarchar` |Unique role code.|
|[Pos_Role_Name](#pos_role_name)|`nvarchar` `ML`|Multi-language name of the POS role.|
|[Can_Void_Sales](#can_void_sales)|`bit` |Indicates whether this role can void sales orders.|
|[Can_Process_Minus_Sales](#can_process_minus_sales)|`bit` |Indicates whether the role is allowed to process minus (qty and/or value) sales.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pos_Role_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pos_Role_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Pos_Role_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Can_Void_Sales

| Property | Value |
| - | - |
|Type|bit|

### Can_Process_Minus_Sales

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


