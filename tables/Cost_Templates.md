# Table Cost_Templates

Cost templates specify how to calculate and allocate costs. Entity: Cost_Templates

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Cost_Template_Id|`Guid`|`PK`, Readonly||
|Cost_Template_Code|`String`||Unique code of the cost template. `Required` `Filter(eq)` |
|Cost_Template_Name|`String`||Name of the cost template. `Required` `Filter(like)` |
