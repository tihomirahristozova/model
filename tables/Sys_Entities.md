# Table Sys_Entities

Contains entities, which have secured access. Entity: Sys_Entities

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Entity_Id|`Guid`|`PK`, Readonly||
|Log_Create|`Boolean`||Specifies whether to log every insert for this entity. `Required` `Default(false)` `Introduced in version 18.2` |
|Log_Delete|`Boolean`||Specifies whether to log every delete for this entity. `Required` `Default(false)` `Introduced in version 18.2` |
|Log_Read_By_Id|`Boolean`||Specifies whether to log every load by Id for this entity. `Required` `Default(false)` `Introduced in version 18.2` |
|Log_Read_Many|`Boolean`||Specifies whether to log every load of many records for this entity. `Required` `Default(false)` `Introduced in version 18.2` |
|Log_Update|`Boolean`||Specifies whether to log every update for this entity. `Required` `Default(false)` `Introduced in version 18.2` |
|Entity_Name|`String`||The system name of the entity, which is being secured. `Required` `Filter(eq;like)` `ORD` |
|Track_Changes_Level|`TrackChangesLevel`|Allowed: `0`, `1`, `2`, `3`, `4`|The track changes level for the entity. `Required` `Default(0)` `Filter(multi eq)` `Introduced in version 19.1` |
