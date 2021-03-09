# Table Prd_Principal_Recipe_Ingredients

Template for material usage of a principal recipe. Entity: Prd_Principal_Recipe_Ingredients

## Owner Tables Hierarchy

* [Prd_Principal_Recipes](Prd_Principal_Recipes.md)
* [Gen_Product_Groups](Gen_Product_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|The Id of the recipe ingredient. This changes for each different line of each different recipe in contrast to the ingredient id, which might be the same for many principal recipes|
|[Principal_Recipe_Id](#principal_recipe_id)|`uniqueidentifier` ||
|[Ingredient_Id](#ingredient_id)|`uniqueidentifier` |The Id of the ingredient. When copying principal recipes, this Id remains the same for the new principal recipe to provide upgrade path for old recipes.|
|[Ingredient_Name](#ingredient_name)|`nvarchar(254)` |The principal name of the ingredient.|
|[Conditional_Property_Id](#conditional_property_id)|`uniqueidentifier` |When not NULL, specifies that, when creating recipe, the ingredient will be added only if this property is set for the main product|
|[Conditional_Property_Value](#conditional_property_value)|`nvarchar(254)` |The desired value of Conditional Property in order for the template line to match.|
|[Conditional_Property_Description](#conditional_property_description)|`nvarchar(254)` `ML`|The desired description of Conditional Property in order for the template line to match.|
|[Conditional_Property_Allowed_Value_Id](#conditional_property_allowed_value_id)|`uniqueidentifier` |When not NULL, specifies that, when creating recipe, the ingredient will be added only if the main product property, specified in Conditional_Property_Id equals the specified value|
|[Material_Group_Id](#material_group_id)|`uniqueidentifier` |Filter for choosing specific material in the recipe (Gen_Product_Groups_Table)|
|[Default_Material_Id](#default_material_id)|`uniqueidentifier` |If not NULL, points to default product for this ingredient|
|[Usage_Quantity](#usage_quantity)|`decimal(18, 6)` |Quantity to be consumed from the material. NULL means that the quantity is specified with formula|
|[Usage_Quantity_Formula](#usage_quantity_formula)|`nvarchar(2147483647)` |Specifies formula for the usage quantity. The formula can reference properties in [<Prop_Name>] style, just like products name and description mask. The formula can contain *, /, + and - operators. The formula can also be simple number, directly specifying quantity|
|[Usage_Unit_Id](#usage_unit_id)|`uniqueidentifier` |The measurement unit of Usage_Quantity. The selected item must support the specified unit|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe.|
|[Line_Ord](#line_ord)|`int` |The position of the line in the recipe model|
|[Material_From_Property_Id](#material_from_property_id)|`uniqueidentifier` |When not NULL, specifies that the material will be obtained from the value of the specified property. The property must have allowed values in the Products domain.|
|[Operation_Id](#operation_id)|`uniqueidentifier` |Specifies for which operation this ingredient will be used|
|[Fixed_Scrap_Quantity](#fixed_scrap_quantity)|`decimal(18, 3)` |Fixed scrap quantity for setup|
|[Default_Store_Id](#default_store_id)|`uniqueidentifier` |The default store from which to retrieve the material.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ingredient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ingredient_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Conditional_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Conditional_Property_Value

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Conditional_Property_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Conditional_Property_Allowed_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Usage_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Usage_Quantity_Formula

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Usage_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Material_From_Property_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fixed_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Default_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


