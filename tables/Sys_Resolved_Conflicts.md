# Table Sys_Resolved_Conflicts

Contains records of conflicts, which were automatically resolved by update procedures. Entity: Sys_Resolved_Conflicts

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Resolved_Conflict_Id|`Guid`|`PK`, Readonly||
|Conflict_Description|`MultilanguageString`|Readonly|Description of the conflict. `Required` `ReadOnly` |
|Resolve_Confirmed_By_User|`Boolean`||True, when the conflict resolution was manually confirmed by user. `Required` `Default(false)` `Filter(eq)` |
|Resolve_Confirmed_Time|`DateTime?`|Readonly|Time when the conflict resolution was confirmed by the user. `ReadOnly` |
|Resolve_Description|`MultilanguageString`|Readonly|Description of the resolution of the conflict. `Required` `ReadOnly` |
|Resolved_Time|`DateTime`|Readonly|Time when the resolution of the conflict was made. `Required` `Default(Now)` `ReadOnly` |
|Revised_By_User|`Boolean`|Readonly|True, when the conflict resolution was revised (reviewed) manually by user. `Required` `Default(false)` `Filter(eq)` `ReadOnly` |
|Table_Name|`MultilanguageString`|Readonly|Name of the table in which the conflict has occurred. `Required` `Filter(like)` `ReadOnly` |
|URL|`String`|Readonly|URL of the item (the row) for which the conflict occurred. `Required` `ReadOnly` |
