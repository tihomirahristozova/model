# Table Inv_Store_Groups

Hierarchy of store groups. Entity: Inv_Store_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Store_Group_Id|`Guid`|`PK`, Readonly||
|Store_Group_Code|`String`||The unique code of the StoreGroup. `Required` `Filter(eq;like)` |
|Full_Path|`String`|Readonly|The full path to the store group in a dot separated, non-leading dot format. For example: 001.005.008. `Filter(eq;like)` `ORD` `ReadOnly` |
|Store_Group_Name|`MultilanguageString`||The name of this StoreGroup. `Required` `Filter(like)` |
|Parent_Full_Path|`String`||The full path to the parent store group. It is stored in a dot separated, non-leading dot format. For example: 001.005. `Filter(eq;like)` |
