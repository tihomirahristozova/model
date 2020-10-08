---
uid: Production.Technologies.RecipeIngredients
---
# Production.Technologies.RecipeIngredients

Contains the materials of a recipe that make up the product. Entity: Prd_Recipe_Ingredients

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Technologies.RecipeIngredients.md#Id) | guid |  
| [Cost](Production.Technologies.RecipeIngredients.md#Cost) | [Amount](../data-types.md#Amount) | The cost of the specified quantity of the ingredient. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)] 
| [FixedScrapQuantity](Production.Technologies.RecipeIngredients.md#FixedScrapQuantity) | [Quantity](../data-types.md#Quantity) | Fixed scrap quantity of the material, needed for setup. [Unit: UsageUnit] [Required] [Default(0)] 
| [LineOrd](Production.Technologies.RecipeIngredients.md#LineOrd) | int32 | The order of this line in the recipe. [Required] 
| [Notes](Production.Technologies.RecipeIngredients.md#Notes) | string (nullable) | Notes for this RecipeIngredient. 
| [Price](Production.Technologies.RecipeIngredients.md#Price) | [Amount](../data-types.md#Amount) | Total price of the ingredient. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)] 
| [ScrapRate](Production.Technologies.RecipeIngredients.md#ScrapRate) | decimal | The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe. [Required] [Default(0)] 
| [UnitCost](Production.Technologies.RecipeIngredients.md#UnitCost) | [Amount](../data-types.md#Amount) | Cost of 1 of Usage_Unit_Id. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)] 
| [UnitPrice](Production.Technologies.RecipeIngredients.md#UnitPrice) | [Amount](../data-types.md#Amount) | Price for 1 of Usage_Unit_Id. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)] 
| [UsageQuantity](Production.Technologies.RecipeIngredients.md#UsageQuantity) | [Quantity](../data-types.md#Quantity) (nullable) | Quantity of the material, consumed in the operation. The measurement unit is the primary unit of Material_Item_Id. [Unit: UsageUnit] [Default(1.000)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Material](Production.Technologies.RecipeIngredients.md#Material) | [General.Products.Products](General.Products.Products.md) | The Id of the consumed material (Gen_Products_Table). [Required] [Filter(multi eq)] |
| [Operation](Production.Technologies.RecipeIngredients.md#Operation) | [Production.Resources.Operations](Production.Resources.Operations.md) (nullable) | Specifies for which operation this ingredient will be used. [Filter(multi eq)] |
| [PrincipalRecipeIngredient](Production.Technologies.RecipeIngredients.md#PrincipalRecipeIngredient) | [Production.Technologies.PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md) (nullable) | The principal recipe ingredient which was used to create this recipe ingredient. null means that this ingredient is standalone, not created with principal recipe ingredient. [Filter(multi eq)] |
| [Recipe](Production.Technologies.RecipeIngredients.md#Recipe) | [Production.Technologies.Recipes](Production.Technologies.Recipes.md) | The [Recipe](Production.Technologies.RecipeIngredients.md#Recipe) to which this RecipeIngredient belongs. [Required] [Filter(multi eq)] [Owner] |
| [Store](Production.Technologies.RecipeIngredients.md#Store) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store from which to retrieve the material. [Filter(multi eq)] |
| [UsageUnit](Production.Technologies.RecipeIngredients.md#UsageUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Usage_Quantity. The selected item must support the specified unit. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Cost

> The cost of the specified quantity of the ingredient. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### FixedScrapQuantity

> Fixed scrap quantity of the material, needed for setup. [Unit: UsageUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### LineOrd

> The order of this line in the recipe. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Recipe.Ingredients.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Recipe.Ingredients.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this RecipeIngredient.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Price

> Total price of the ingredient. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### ScrapRate

> The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### UnitCost

> Cost of 1 of Usage_Unit_Id. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### UnitPrice

> Price for 1 of Usage_Unit_Id. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### UsageQuantity

> Quantity of the material, consumed in the operation. The measurement unit is the primary unit of Material_Item_Id. [Unit: UsageUnit] [Default(1.000)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity) (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### Material

> The Id of the consumed material (Gen_Products_Table). [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Operation

> Specifies for which operation this ingredient will be used. [Filter(multi eq)]

_Type_: **[Production.Resources.Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PrincipalRecipeIngredient

> The principal recipe ingredient which was used to create this recipe ingredient. null means that this ingredient is standalone, not created with principal recipe ingredient. [Filter(multi eq)]

_Type_: **[Production.Technologies.PrincipalRecipeIngredients](Production.Technologies.PrincipalRecipeIngredients.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Recipe

> The [Recipe](Production.Technologies.RecipeIngredients.md#Recipe) to which this RecipeIngredient belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Technologies.Recipes](Production.Technologies.Recipes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Store

> The store from which to retrieve the material. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### UsageUnit

> The measurement unit of Usage_Quantity. The selected item must support the specified unit. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Technologies.RecipeIngredients erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Technologies.RecipeIngredients erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Technologies.RecipeIngredients erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_RecipeIngredients?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_RecipeIngredients?$top=10>

