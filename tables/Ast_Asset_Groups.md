# Table Ast_Asset_Groups

User-defined grouping of the assets. Entity: Ast_Asset_Groups

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Asset_Group_Id|`Guid`|`PK`, Readonly||
|Asset_Group_Code|`String`||The unique code of the AssetGroup. `Required` `Filter(eq)` `ORD` |
|Asset_Group_Name|`String`||The name of this AssetGroup. `Required` `Filter(like)` |
