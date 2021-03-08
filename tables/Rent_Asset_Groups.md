# Table Rent_Asset_Groups

Groups the rentable assets in hierarchy of logical groups. Entity: Rent_Asset_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Rental_Asset_Group_Id|`Guid`|`PK`, Readonly||
|Full_Path|`String`|Readonly|The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. `ORD` `ReadOnly` |
|Notes|`String`||Notes for this AssetGroup. |
|Parent_Full_Path|`String`||The full path of the parent node. `Filter(eq)` |
|Rental_Asset_Group_Code|`String`||Asset group code, unique within the parent node. `Required` `Filter(eq;like)` |
|Rental_Asset_Group_Name|`String`||Asset group name, unique within the parent node. `Required` `Filter(eq;like)` |
