# Table Prd_Operation_Groups

Groups of operations. Entity: Prd_Operation_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Full_Path|`String`||The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. `Required` `Default("")` `Filter(like)` |
|Operation_Group_Name|`String`||The name of this OperationGroup. `Required` `Filter(like)` |
|Parent|`String`||Path of parent group. `Required` `Default("/")` `Filter(like)` `ORD` |
