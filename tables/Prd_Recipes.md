# Table Prd_Recipes

Contains the characteristics of operations used to create products. Entity: Prd_Recipes

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Creation_Time|`DateTime?`|Readonly|Date and time when the Recipe was created. `Filter(ge;le)` `ReadOnly` |
|Creation_User|`String`|Readonly|Login name of the user, who created the Recipe. `Filter(like)` `ReadOnly` |
|Expiry_Date|`DateTime?`||The last date, when the recipe should be used. null means that the recipe might still be in use. `Filter(ge;le)` |
|Is_Default|`Boolean`||Default for period: Release_Date - Expiry_Date. `Required` `Default(false)` `Filter(eq)` |
|Recipe_Name|`String`||The name of the recipe. When there is only 1 recipe, it is often equal to the product name. However, when there are multiple recipes for one product, the name is used for diferentiation. `Required` `Filter(like)` |
|Notes|`String`||User comments for the recipe. |
|Release_Date|`DateTime`||The date, when the recipe was released to production. `Required` `Default(Today)` `Filter(ge;le)` |
|Scrap_Rate|`Decimal`||The percentage (0..1) of scrap usually occurring during the operation. Specifying this leads to inflated requirements of all raw materials for this recipe. `Required` `Default(0)` |
|Update_Time|`DateTime?`|Readonly|Date and time when the Recipe was last updated. `Filter(ge;le)` `ReadOnly` |
|Update_User|`String`|Readonly|Login name of the user, who last updated the Recipe. `Filter(like)` `ReadOnly` |
