# Query Sys_Objects_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Id](#object_id)|`uniqueidentifier` `PK`|.|
|[Entity_Type](#entity_type)|`nvarchar` |The entity type of the row to which the object is bound|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The Id of the primary row to which the object is bound|
|[Latest_Version](#latest_version)|`int` |The latest saved version of the object. Starts from 1 and increments with 1 for each new version.|
|[Row_Version](#row_version)|`timestamp` ||
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC) when the object represented by this system object was created. NULL means that it is unknown.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the object represented by this system object . NULL means that it is unknown.|
|[Last_Update_Time_Utc](#last_update_time_utc)|`datetime` |The exact server time (in UTC) of the last modification of the object represented by this system object. NULL means that it is unknown.|
|[Last_Update_User_Id](#last_update_user_id)|`uniqueidentifier` |The user, who made the last modification of the object represented by this system object . NULL means that it is unknown.|
|[Is_Deleted](#is_deleted)|`bit` |Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes.|

## Columns

### Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Entity_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Latest_Version

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Creation_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Last_Update_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Last_Update_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Deleted

| Property | Value |
| - | - |
|Type|bit|


