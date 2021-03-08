# Table Prd_Principal_Recipe_Ingredients

Template for material usage of a principal recipe. Entity: Prd_Principal_Recipe_Ingredients

# Aggregate Hierarchy

* [Prd_Principal_Recipes](Prd_Principal_Recipes.md)
* [Gen_Product_Groups](Gen_Product_Groups.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Id|`Guid`|`PK`, Readonly||
|Conditional_Property_Description|`MultilanguageString`||The desired description of Conditional Property in order for the template line to match. |
|Conditional_Property_Value|`String`||The desired value of Conditional Property in order for the template line to match. |
|Ingredient_Name|`String`||The principal name of the ingredient. `Required` `Filter(like)` |
|Line_Ord|`Int32`||The position of the line in the recipe model. `Required` |
|Scrap_Rate|`Decimal`||The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe. `Required` `Default(0)` `Filter(ge;le)` |
|Usage_Quantity_Formula|`String`||Specifies formula for the usage quantity. The formula can reference properties in `<Prop_Name>` style, just like products name and description mask. The formula can contain *, /, + and - operators. The formula can also be simple number, directly specifying quantity. |
