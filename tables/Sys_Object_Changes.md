# Table Sys_Object_Changes

Actual tracked changes to one object. Entity: Sys_Object_Changes (Introduced in version 19.1)

# Aggregate Hierarchy

* [Sys_Object_Changesets](Sys_Object_Changesets.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Object_Change_Id|`Guid`|`PK`, Readonly||
|Change_Type|`ChangeType`|Allowed: `C`, `U`, `D`|Type of change - Create, Update or Delete. `Required` |
|Entity_Item_Id|`Guid`||The id of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. `Required` `Filter(multi eq)` |
|Repository_Name|`String`||The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. `Required` `Filter(multi eq;like)` |
