# Query Sec_Access_Keys_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` `PK`||
|[Entity_Name](#entity_name)|`nvarchar` |What entitity the key secures. Can be null for private, legacy keys|
|[Access_Key_Code](#access_key_code)|`nvarchar` |Unique code for the access key. The codes can be null for legacy keys or entities that do not support codes. The codes are unique only among non-null entries|
|[Access_Key_Name](#access_key_name)|`nvarchar` `ML`|Multilanguage descriptive name of the security key. Can be null for legacy keys|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Access_Key_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Access_Key_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Access_Key_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


