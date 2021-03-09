# Table Scm_Supplier_Types

Supplier types are primarily used to differentiate the security level access to the different supplier groups. Entity: Scm_Supplier_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Supplier_Type_Id](#supplier_type_id)|`uniqueidentifier` `PK`||
|[Supplier_Type_Name](#supplier_type_name)|`nvarchar(254)` ||
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |The access key required for accessing all suppliers of this supplier type.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Supplier_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Supplier_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


