# Table Cost_Template_Cost_Types

Contains the cost types and their hierachy positions within a cost calculation. Entity: Cost_Template_Cost_Types

# Aggregate Hierarchy

* [Cost_Templates](Cost_Templates.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Template_Cost_Type_Id|`Guid`|`PK`, Readonly||
|Hierarchy_Level|`Int32`||The level in the hierarchy on which this cost is incurred (0..9). `Required` `Filter(ge;le)` |
