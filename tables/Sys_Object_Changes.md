# Table Sys_Object_Changes

Actual tracked changes to one object. Entity: Sys_Object_Changes (Introduced in version 19.1)

## Owner Tables Hierarchy

* [Sys_Object_Changesets](Sys_Object_Changesets.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Object_Change_Id](#object_change_id)|`uniqueidentifier` `PK`||
|[Object_Changeset_Id](#object_changeset_id)|`uniqueidentifier` |The changeset containing this change.|
|[Root_Object_Id](#root_object_id)|`uniqueidentifier` |The root object in the aggregate of the object, which has been changed. Each change is recorded at the aggregate root level.|
|[Repository_Name](#repository_name)|`nvarchar(64)` |The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Entity_Item_Id](#entity_item_id)|`uniqueidentifier` |The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object.|
|[Change_Type](#change_type)|`nvarchar(1)` Allowed: `C`, `U`, `D`|Type of change - Create, Update or Delete.|
|[Old_Values_Json](#old_values_json)|`nvarchar(2147483647)` |Old values in a name-value Json format. Only changed data attributes are recorded. Old values are recorded for update and delete.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Object_Change_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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
|Type|nvarchar(64)|

### Entity_Item_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Change_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Old_Values_Json

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


