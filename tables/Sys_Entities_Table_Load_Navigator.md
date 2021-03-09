# Query Sys_Entities_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Entity_Id](#entity_id)|`uniqueidentifier` `PK`||
|[Entity_Name](#entity_name)|`nvarchar` |The system name of the entity, which is being secured.|
|[Access_Key_Id](#access_key_id)|`uniqueidentifier` |The access key, required to access the secured entity.|
|[Row_Version](#row_version)|`timestamp` ||
|[Log_Read_Many](#log_read_many)|`bit` |Specifies whether to log every load of many records for this entity.|
|[Log_Read_By_Id](#log_read_by_id)|`bit` |Specifies whether to log every load by Id for this entity.|
|[Log_Update](#log_update)|`bit` |Specifies whether to log every update for this entity.|
|[Log_Delete](#log_delete)|`bit` |Specifies whether to log every delete for this entity.|
|[Log_Create](#log_create)|`bit` ||
|[Track_Changes_Level](#track_changes_level)|`tinyint` Allowed: `0`, `1`, `2`, `3`, `4`||

## Columns

### Entity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Name

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

### Log_Read_Many

| Property | Value |
| - | - |
|Type|bit|

### Log_Read_By_Id

| Property | Value |
| - | - |
|Type|bit|

### Log_Update

| Property | Value |
| - | - |
|Type|bit|

### Log_Delete

| Property | Value |
| - | - |
|Type|bit|

### Log_Create

| Property | Value |
| - | - |
|Type|bit|

### Track_Changes_Level

| Property | Value |
| - | - |
|Type|tinyint|


