# Table Cost_Template_Levels

Represents named hierarchy levels within a cost calculation. The hierarchy levels are used to specify cost allocation mechanisms. Entity: Cost_Template_Levels

# Aggregate Hierarchy

* [Cost_Templates](Cost_Templates.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Template_Level_Id|`Guid`|`PK`, Readonly||
|Hierarchy_Level|`Int32`||The level within the hierarchy 0=Root, 1=one level below root, etc. (0..9). `Required` `Default(0)` `Filter(ge;le)` |
|Level_Name|`String`||The name of the hierarchy level. `Required` `Filter(like)` |
