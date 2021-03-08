# Table Prd_Recipe_Ingredients

Contains the materials of a recipe that make up the product. Entity: Prd_Recipe_Ingredients

# Aggregate Hierarchy

* [Prd_Recipes](Prd_Recipes.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Line_Ord|`Int32`||The order of this line in the recipe. `Required` |
|Notes|`String`||Notes for this RecipeIngredient. |
|Scrap_Rate|`Decimal`||The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe. `Required` `Default(0)` |
