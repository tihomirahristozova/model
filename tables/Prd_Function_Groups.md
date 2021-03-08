# Table Prd_Function_Groups

Represents the hierarchy of the function groups. They group the multitude of resource functions in logical, user-defined groups. Entity: Prd_Function_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Full_Path|`String`||The full path of the item. `Required` `Default("")` `Filter(eq;like)` |
|Function_Group_Name|`String`||The name of this FunctionGroup. `Required` `Filter(like)` |
|Parent|`String`||The path of the parent item. `Required` `Default("/")` `Filter(eq;like)` `ORD` |
