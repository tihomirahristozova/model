# Table Prd_Recipe_Ingredients

Contains the materials of a recipe that make up the product. Entity: Prd_Recipe_Ingredients

## Owner Tables Hierarchy

* [Prd_Recipes](Prd_Recipes.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |The order of this line in the recipe.|
|[Material_Id](#material_id)|`uniqueidentifier` |The Id of the consumed material (Gen_Products_Table)|
|[Usage_Quantity](#usage_quantity)|`decimal(18, 6)` |Quantity of the material, consumed in the operation. The measurement unit is the primary unit of Material_Item_Id.|
|[Usage_Unit_Id](#usage_unit_id)|`uniqueidentifier` |The measurement unit of Usage_Quantity. The selected item must support the specified unit|
|[Unit_Price](#unit_price)|`decimal(18, 6)` |Price for 1 of Usage_Unit_Id|
|[Price](#price)|`decimal(18, 4)` |Total price of the ingredient|
|[Unit_Cost](#unit_cost)|`decimal(18, 6)` |Cost of 1 of Usage_Unit_Id|
|[Cost](#cost)|`decimal(18, 4)` |The cost of the specified quantity of the ingredient|
|[Store_Id](#store_id)|`uniqueidentifier` |The store from which to retrieve the material.|
|[Scrap_Rate](#scrap_rate)|`decimal(7, 6)` |The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe|
|[Notes](#notes)|`nvarchar(254)` ||
|[Operation_Id](#operation_id)|`uniqueidentifier` |Specifies for which operation this ingredient will be used|
|[Id](#id)|`uniqueidentifier` `PK`||
|[Principal_Recipe_Ingredient_Id](#principal_recipe_ingredient_id)|`uniqueidentifier` |The principal recipe ingredient which was used to create this recipe ingredient. NULL means that this ingredient is standalone, not created with principal recipe ingredient|
|[Recipe_Id](#recipe_id)|`uniqueidentifier` ||
|[Fixed_Scrap_Quantity](#fixed_scrap_quantity)|`decimal(18, 3)` |Fixed scrap quantity of the material, needed for setup.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Usage_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Usage_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Unit_Price

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Price

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Cost

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Scrap_Rate

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Operation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Principal_Recipe_Ingredient_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fixed_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


