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


Id


The Id of the recipe ingredient. This changes for each different line of each different recipe in contrast to the ingredient id, which might be the same for many principal recipes


The Id of the recipe ingredient. This changes for each different line of each different recipe in contrast to the ingredient id, which might be the same for many principal recipes

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Id](Prd_Principal_Recipe_Ingredients.md#id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Principal_Recipe_Id


Principal_Recipe_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Prd_Principal_Recipes](Prd_Principal_Recipes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Principal_Recipe_Id](Prd_Principal_Recipe_Ingredients.md#principal_recipe_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Ingredient_Id


Ingredient_Id


The Id of the ingredient. When copying principal recipes, this Id remains the same for the new principal recipe to provide upgrade path for old recipes.


The Id of the ingredient. When copying principal recipes, this Id remains the same for the new principal recipe to provide upgrade path for old recipes.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Ingredient_Id](Prd_Principal_Recipe_Ingredients.md#ingredient_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Ingredient_Name


Ingredient_Name


The principal name of the ingredient.


The principal name of the ingredient.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Ingredient_Name](Prd_Principal_Recipe_Ingredients.md#ingredient_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Conditional_Property_Id


Conditional_Property_Id


When not NULL, specifies that, when creating recipe, the ingredient will be added only if this property is set for the main product


When not NULL, specifies that, when creating recipe, the ingredient will be added only if this property is set for the main product

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Conditional_Property_Id](Prd_Principal_Recipe_Ingredients.md#conditional_property_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Conditional_Property_Value


Conditional_Property_Value


The desired value of Conditional Property in order for the template line to match.


The desired value of Conditional Property in order for the template line to match.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Conditional_Property_Value](Prd_Principal_Recipe_Ingredients.md#conditional_property_value)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Conditional_Property_Description


Conditional_Property_Description


The desired description of Conditional Property in order for the template line to match.


The desired description of Conditional Property in order for the template line to match.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Conditional_Property_Description](Prd_Principal_Recipe_Ingredients.md#conditional_property_description)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Conditional_Property_Allowed_Value_Id


Conditional_Property_Allowed_Value_Id


When not NULL, specifies that, when creating recipe, the ingredient will be added only if the main product property, specified in Conditional_Property_Id equals the specified value


When not NULL, specifies that, when creating recipe, the ingredient will be added only if the main product property, specified in Conditional_Property_Id equals the specified value

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Property_Allowed_Values](Gen_Property_Allowed_Values.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Conditional_Property_Allowed_Value_Id](Prd_Principal_Recipe_Ingredients.md#conditional_property_allowed_value_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Material_Group_Id


Material_Group_Id


Filter for choosing specific material in the recipe (Gen_Product_Groups_Table)


Filter for choosing specific material in the recipe (Gen_Product_Groups_Table)

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Product_Groups](Gen_Product_Groups.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Material_Group_Id](Prd_Principal_Recipe_Ingredients.md#material_group_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Default_Material_Id


Default_Material_Id


If not NULL, points to default product for this ingredient


If not NULL, points to default product for this ingredient

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Default_Material_Id](Prd_Principal_Recipe_Ingredients.md#default_material_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Usage_Quantity


Usage_Quantity


Quantity to be consumed from the material. NULL means that the quantity is specified with formula


Quantity to be consumed from the material. NULL means that the quantity is specified with formula

| Property | Value |
| - | - |
|Type|decimal(18, 6)|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Usage_Quantity](Prd_Principal_Recipe_Ingredients.md#usage_quantity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Usage_Quantity_Formula


Usage_Quantity_Formula


Specifies formula for the usage quantity. The formula can reference properties in [<Prop_Name>] style, just like products name and description mask. The formula can contain *, /, + and - operators. The formula can also be simple number, directly specifying quantity


Specifies formula for the usage quantity. The formula can reference properties in [<Prop_Name>] style, just like products name and description mask. The formula can contain *, /, + and - operators. The formula can also be simple number, directly specifying quantity

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Usage_Quantity_Formula](Prd_Principal_Recipe_Ingredients.md#usage_quantity_formula)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Usage_Unit_Id


Usage_Unit_Id


The measurement unit of Usage_Quantity. The selected item must support the specified unit


The measurement unit of Usage_Quantity. The selected item must support the specified unit

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Usage_Unit_Id](Prd_Principal_Recipe_Ingredients.md#usage_unit_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Scrap_Rate


Scrap_Rate


The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe.


The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe.

| Property | Value |
| - | - |
|Type|decimal(7, 6)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsPercent|
|Default Value|0|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Scrap_Rate](Prd_Principal_Recipe_Ingredients.md#scrap_rate)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Line_Ord


Line_Ord


The position of the line in the recipe model


The position of the line in the recipe model

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|1|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Line_Ord](Prd_Principal_Recipe_Ingredients.md#line_ord)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Material_From_Property_Id


Material_From_Property_Id


When not NULL, specifies that the material will be obtained from the value of the specified property. The property must have allowed values in the Products domain.


When not NULL, specifies that the material will be obtained from the value of the specified property. The property must have allowed values in the Products domain.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Properties](Gen_Properties.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Material_From_Property_Id](Prd_Principal_Recipe_Ingredients.md#material_from_property_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Operation_Id


Operation_Id


Specifies for which operation this ingredient will be used


Specifies for which operation this ingredient will be used

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Prd_Operations](Prd_Operations.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Operation_Id](Prd_Principal_Recipe_Ingredients.md#operation_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Fixed_Scrap_Quantity


Fixed_Scrap_Quantity


Fixed scrap quantity for setup


Fixed scrap quantity for setup

| Property | Value |
| - | - |
|Type|decimal(18, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Fixed_Scrap_Quantity](Prd_Principal_Recipe_Ingredients.md#fixed_scrap_quantity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Default_Store_Id


Default_Store_Id


The default store from which to retrieve the material.


The default store from which to retrieve the material.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Default_Store_Id](Prd_Principal_Recipe_Ingredients.md#default_store_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Prd_Principal_Recipe_Ingredients](Prd_Principal_Recipe_Ingredients.md).[Row_Version](Prd_Principal_Recipe_Ingredients.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


