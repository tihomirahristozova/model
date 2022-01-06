---
uid: Production.Technologies.PrincipalRecipes
---
# Production.Technologies.PrincipalRecipes Entity

**Namespace:** [Production.Technologies](Production.Technologies.md)  

List of base recipe models. Recipe models are used by the Product Configurator to create specific recipes. Entity: Prd_Principal_Recipes

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  
Aggregate Root:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DurationHour](Production.Technologies.PrincipalRecipes.md#durationhour) | decimal (10, 0) | The approximate duration of the operation (for the specified quantities) in seconds. This is pure operation time and excludes setup time. `Required` `Default(0)` 
| [ExpiryDate](Production.Technologies.PrincipalRecipes.md#expirydate) | datetime __nullable__ | The last date, when the recipe should be used. null means that there is no expiry date yet and the recipe model is still active. `Filter(ge;le)` 
| [Id](Production.Technologies.PrincipalRecipes.md#id) | guid |  
| [Name](Production.Technologies.PrincipalRecipes.md#name) | string (64) | Name of the principal recipe. `Required` `Filter(like)` 
| [Notes](Production.Technologies.PrincipalRecipes.md#notes) | string (254) __nullable__ | User comments for the principal recipe. 
| [ObjectVersion](Production.Technologies.PrincipalRecipes.md#objectversion) | int32 |  
| [ProduceQuantity](Production.Technologies.PrincipalRecipes.md#producequantity) | [Quantity (18, 3)](../data-types.md#quantity) | Suggested quantity to produce. Usually it is equal to 1. `Unit: ProduceUnit` `Required` `Default(1)` `Filter(ge;le)` 
| [ReleaseDate](Production.Technologies.PrincipalRecipes.md#releasedate) | datetime | The date, when the recipe model is released for use. `Required` `Default(Today)` `Filter(ge;le)` 
| [ScrapRate](Production.Technologies.PrincipalRecipes.md#scraprate) | decimal (7, 6) | The percentage (0..1) of scrap usually occurring during the production operations. Specifying this leads to inflated requirements of all raw materials for the recipe. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProduceUnit](Production.Technologies.PrincipalRecipes.md#produceunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Produce_Quantity. The selected item must support the specified unit. `Required` `Filter(multi eq)` |
| [ProductGroup](Production.Technologies.PrincipalRecipes.md#productgroup) | [ProductGroups](General.Products.ProductGroups.md) | The production group, whose production is defined by the principal recipe . `Required` `Filter(multi eq)` `Owner` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Ingredients | [PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md) | List of `PrincipalRecipe<br />Ingredient`(Production.Technologies.PrincipalRecipeIngredients.md) child objects, based on the `Production.Technologies.PrincipalRecipeIngredient.PrincipalRecipe`(Production.Technologies.PrincipalRecipeIngredients.md#principalrecipe) back reference 
| Operations | [PrincipalRecipeOperations](Production.Technologies.PrincipalRecipeOperations.md) | List of `PrincipalRecipeOperation`(Production.Technologies.PrincipalRecipeOperations.md) child objects, based on the `Production.Technologies.PrincipalRecipeOperation.PrincipalRecipe`(Production.Technologies.PrincipalRecipeOperations.md#principalrecipe) back reference 


## Attribute Details

### DurationHour

The approximate duration of the operation (for the specified quantities) in seconds. This is pure operation time and excludes setup time. `Required` `Default(0)`

_Type_: **decimal (10, 0)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ExpiryDate

The last date, when the recipe should be used. null means that there is no expiry date yet and the recipe model is still active. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the principal recipe. `Required` `Filter(like)`

_Type_: **string (64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Notes

User comments for the principal recipe.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ProduceQuantity

Suggested quantity to produce. Usually it is equal to 1. `Unit: ProduceUnit` `Required` `Default(1)` `Filter(ge;le)`

_Type_: **[Quantity (18, 3)](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ReleaseDate

The date, when the recipe model is released for use. `Required` `Default(Today)` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDate**  

### ScrapRate

The percentage (0..1) of scrap usually occurring during the production operations. Specifying this leads to inflated requirements of all raw materials for the recipe. `Required` `Default(0)`

_Type_: **decimal (7, 6)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### ProduceUnit

The measurement unit of Produce_Quantity. The selected item must support the specified unit. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductGroup

The production group, whose production is defined by the principal recipe . `Required` `Filter(multi eq)` `Owner`

_Type_: **[ProductGroups](General.Products.ProductGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Production.Technologies.PrincipalRecipes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Production.Technologies.PrincipalRecipes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_PrincipalRecipes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_PrincipalRecipes?$top=10>

