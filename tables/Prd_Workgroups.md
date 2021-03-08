# Table Prd_Workgroups

Production workgroups. Entity: Prd_Workgroups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Full_Path|`String`||The full path to the current node, represented with slash ('/') as leading, trailing and separator character. Example: '/rootnode/subnode/'. `Default("")` |
|Workgroup_Name|`String`||Name of the workgroup. `Required` `Filter(like)` |
|Notes|`String`||User notes for the workgroup. |
|Parent|`String`||Path-like parent workgroup name. `Required` `Default("/")` `Filter(like)` `ORD` |
