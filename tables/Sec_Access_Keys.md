# Table Sec_Access_Keys

Access keys provide the basic locking mechanism for data security. Each record can be secured by specifying an access key. Then the users are given access to access keys through groups. Entity: Sec_Access_Keys

## Summary

| Name | Type | Description |
| - | - | --- |
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` `PK`||
|[Entity_Name](#entity_name)|`nvarchar(64)` |What entitity the key secures. Can be null for private, legacy keys|
|[Access_Key_Code](#access_key_code)|`nvarchar(16)` |Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries|
|[Access_Key_Name](#access_key_name)|`nvarchar(1024)` `ML`|Multilanguage descriptive name of the security key. Can be null for legacy keys|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Access_Key_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Access_Key_Name

| Property | Value |
| - | - |
|Type|nvarchar(1024)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


