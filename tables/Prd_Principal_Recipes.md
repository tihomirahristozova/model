# Table Prd_Principal_Recipes

List of base recipe models. Recipe models are used by the Product Configurator to create specific recipes. Entity: Prd_Principal_Recipes

# Aggregate Hierarchy

* [Gen_Product_Groups](Gen_Product_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Duration_Hour|`Decimal`||The approximate duration of the operation (for the specified quantities) in seconds. This is pure operation time and excludes setup time. `Required` `Default(0)` |
|Expiry_Date|`DateTime?`||The last date, when the recipe should be used. null means that there is no expiry date yet and the recipe model is still active. `Filter(ge;le)` |
|Principal_Recipe_Name|`String`||Name of the principal recipe. `Required` `Filter(like)` |
|Notes|`String`||User comments for the principal recipe. |
|Release_Date|`DateTime`||The date, when the recipe model is released for use. `Required` `Default(Today)` `Filter(ge;le)` |
|Scrap_Rate|`Decimal`||The percentage (0..1) of scrap usually occurring during the production operations. Specifying this leads to inflated requirements of all raw materials for the recipe. `Required` `Default(0)` |
