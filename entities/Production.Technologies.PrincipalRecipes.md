---
uid: Production.Technologies.PrincipalRecipes
---
# Production.Technologies.PrincipalRecipes Entity

List of base recipe models. Recipe models are used by the Product Configurator to create specific recipes. Entity: Prd_Principal_Recipes

Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DurationHour](Production.Technologies.PrincipalRecipes.md#durationhour) | decimal | The approximate duration of the operation (for the specified quantities) in seconds. This is pure operation time and excludes setup time. [Required] [Default(0)] 
| [ExpiryDate](Production.Technologies.PrincipalRecipes.md#expirydate) | datetime (nullable) | The last date, when the recipe should be used. null means that there is no expiry date yet and the recipe model is still active. [Filter(ge;le)] 
| [Id](Production.Technologies.PrincipalRecipes.md#id) | guid |  
| [Name](Production.Technologies.PrincipalRecipes.md#name) | string | Name of the principal recipe. [Required] [Filter(like)] 
| [Notes](Production.Technologies.PrincipalRecipes.md#notes) | string (nullable) | User comments for the principal recipe. 
| [ProduceQuantity](Production.Technologies.PrincipalRecipes.md#producequantity) | [Quantity](../data-types.md#quantity) | Suggested quantity to produce. Usually it is equal to 1. [Unit: ProduceUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [ReleaseDate](Production.Technologies.PrincipalRecipes.md#releasedate) | datetime | The date, when the recipe model is released for use. [Required] [Default(Today)] [Filter(ge;le)] 
| [ScrapRate](Production.Technologies.PrincipalRecipes.md#scraprate) | decimal | The percentage (0..1) of scrap usually occurring during the production operations. Specifying this leads to inflated requirements of all raw materials for the recipe. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProduceUnit](Production.Technologies.PrincipalRecipes.md#produceunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Produce_Quantity. The selected item must support the specified unit. [Required] [Filter(multi eq)] |
| [ProductGroup](Production.Technologies.PrincipalRecipes.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) | The production group, whose production is defined by the principal recipe . [Required] [Filter(multi eq)] [Owner] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Ingredients | [PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md) | List of [PrincipalRecipe<br />Ingredient](Production.Technologies.PrincipalRecipeIngredients.md) child objects, based on the [Production.Technologies.PrincipalRecipeIngredient.PrincipalRecipe](Production.Technologies.PrincipalRecipeIngredients.md#principalrecipe) back reference 
| Operations | [PrincipalRecipeOperations](Production.Technologies.PrincipalRecipeOperations.md) | List of [PrincipalRecipeOperation](Production.Technologies.PrincipalRecipeOperations.md) child objects, based on the [Production.Technologies.PrincipalRecipeOperation.PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#principalrecipe) back reference 


## Attribute Details

### DurationHour

The approximate duration of the operation (for the specified quantities) in seconds. This is pure operation time and excludes setup time. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ExpiryDate

The last date, when the recipe should be used. null means that there is no expiry date yet and the recipe model is still active. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the principal recipe. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

User comments for the principal recipe.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProduceQuantity

Suggested quantity to produce. Usually it is equal to 1. [Unit: ProduceUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ReleaseDate

The date, when the recipe model is released for use. [Required] [Default(Today)] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### ScrapRate

The percentage (0..1) of scrap usually occurring during the production operations. Specifying this leads to inflated requirements of all raw materials for the recipe. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### ProduceUnit

The measurement unit of Produce_Quantity. The selected item must support the specified unit. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductGroup

The production group, whose production is defined by the principal recipe . [Required] [Filter(multi eq)] [Owner]

_Type_: **[ProductGroups](General.Products.ProductGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_PrincipalRecipes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_PrincipalRecipes?$top=10>

