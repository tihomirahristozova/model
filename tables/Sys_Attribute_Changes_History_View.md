# View Sys_Attribute_Changes_History_View

Each entry represents an entity attribute change with previous and new value. Entity: Sys_Attribute_Changes_History_View

## Summary

| Name | Type | Description |
| - | - | --- |
|[Repository_Name](#repository_name)|`nvarchar(64)` |The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The id of the actual changed object, described by this change.|
|[Attribute_Name](#attribute_name)|`nvarchar(64)` ||
|[New_Value](#new_value)|`nvarchar(2147483647)` |The new value|
|[Previous_Value](#previous_value)|`nvarchar(2147483647)` |The previous value|
|[Time_Utc](#time_utc)|`datetime` |Date and time (in Utc) when the changeset was processed by the server.|
|[User_Id](#user_id)|`uniqueidentifier` |The user which initiated the change. NULL when it is unknown.|

## Columns

### Repository_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Attribute_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### New_Value

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Previous_Value

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


