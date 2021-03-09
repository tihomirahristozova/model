# Query Sys_Attribute_Changes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Time_Utc](#time_utc)|`datetime` |Date and time (in Utc) when the changeset was processed by the server.|
|[User_Id](#user_id)|`uniqueidentifier` |The user which initiated the change. NULL when it is unknown.|
|[Application_Name](#application_name)|`nvarchar` |The application which requested the change. NULL when it is unknown.|
|[Server_Version](#server_version)|`nvarchar` |The version of the application server at the time of the change.|
|[Object_Changeset_Id](#object_changeset_id)|`uniqueidentifier` |The changeset containing this change.|
|[Root_Object_Id](#root_object_id)|`uniqueidentifier` |The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level.|
|[Repository_Name](#repository_name)|`nvarchar` |The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Change_Type](#change_type)|`nvarchar` Allowed: `C`, `U`, `D`|Type of change - Create, Update or Delete.|
|[Old_Values_Json](#old_values_json)|`nvarchar` |Old values in a name-value Json format. Only changed data attributes are recorded. Old values are recorded for update and delete.|
|[Object_Change_Id](#object_change_id)|`uniqueidentifier` `PK`||
|[Attribute_Name](#attribute_name)|`nvarchar` `PK`||
|[New_Value](#new_value)|`nvarchar` ||
|[Entity_Type](#entity_type)|`nvarchar` |The entity type of the row to which the object is bound|
|[Object_Entity_Item_Id](#object_entity_item_id)|`uniqueidentifier` |The Id of the primary row to which the object is bound|
|[Latest_Version](#latest_version)|`int` |The latest saved version of the object. Starts from 1 and increments with 1 for each new version.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact server time (in UTC) when the object represented by this system object was created. NULL means that it is unknown.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the object represented by this system object . NULL means that it is unknown.|
|[Last_Update_Time_Utc](#last_update_time_utc)|`datetime` |The exact server time (in UTC) of the last modification of the object represented by this system object. NULL means that it is unknown.|
|[Last_Update_User_Id](#last_update_user_id)|`uniqueidentifier` |The user, who made the last modification of the object represented by this system object . NULL means that it is unknown.|
|[Is_Deleted](#is_deleted)|`bit` |Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes.|

## Columns

### Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Application_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Server_Version

| Property | Value |
| - | - |
|Type|nvarchar|

### Object_Changeset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Root_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Repository_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Change_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Old_Values_Json

| Property | Value |
| - | - |
|Type|nvarchar|

### Object_Change_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Attribute_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### New_Value

| Property | Value |
| - | - |
|Type|nvarchar|

### Entity_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Object_Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Latest_Version

| Property | Value |
| - | - |
|Type|int|

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


