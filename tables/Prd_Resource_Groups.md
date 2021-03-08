# Table Prd_Resource_Groups

Groups of resource types. Entity: Prd_Resource_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Full_Path|`String`||The full path to the operation group. The full path starts with, ends with and is delimited by the "/" (forward slash) character. `Required` `Default("")` `Filter(like)` |
|Resource_Group_Name|`String`||Name of resource group. `Required` `Filter(like)` |
|Parent|`String`||Dot-separated list of parent groups. It also contains leading and trailing dot. `Required` `Default("/")` `Filter(like)` `ORD` |
