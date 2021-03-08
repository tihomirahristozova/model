# Table Cost_Types

Types of costs. Entity: Cost_Types

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Type_Id|`Guid`|`PK`, Readonly||
|Cost_Type_Code|`String`||Unique cost type code. Used for charting. `Required` `Filter(eq)` `ORD` |
|Cost_Type_Name|`String`||Multilanguage cost type name. `Required` `Filter(like)` |
