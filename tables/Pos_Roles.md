# Table Pos_Roles

Represents a role, which can be assigned to POS operators (like Cashier, Manager, etc.). The role indicates the operations, which are allowed to be performed by the operators. Entity: Pos_Roles (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pos_Role_Id](#pos_role_id)|`uniqueidentifier` `PK`||
|[Pos_Role_Code](#pos_role_code)|`nvarchar(16)` |Unique role code.|
|[Pos_Role_Name](#pos_role_name)|`nvarchar(254)` `ML`|Multi-language name of the POS role.|
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
|Type|nvarchar(16)|

### Pos_Role_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

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


