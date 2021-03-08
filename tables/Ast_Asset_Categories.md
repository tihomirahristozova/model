# Table Ast_Asset_Categories

Categorization of the assets, which specifies their depreciation plans. Entity: Ast_Asset_Categories

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Asset_Category_Id|`Guid`|`PK`, Readonly||
|Asset_Category_Code|`String`||The unique code of the AssetCategory. `Required` `Filter(eq)` `ORD` |
|Asset_Category_Name|`String`||The name of this AssetCategory. `Required` `Filter(like)` |
