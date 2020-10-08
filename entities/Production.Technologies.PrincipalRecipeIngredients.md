---
uid: Production.Technologies.PrincipalRecipeIngredients
---
# Production.Technologies.PrincipalRecipeIngredients

Template for material usage of a principal recipe. Entity: Prd_Principal_Recipe_Ingredients

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Technologies.PrincipalRecipeIngredients.md#Id) | guid |  
| [ConditionalPropertyDescription](Production.Technologies.PrincipalRecipeIngredients.md#ConditionalPropertyDescription) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The desired description of Conditional Property in order for the template line to match. 
| [ConditionalPropertyValue](Production.Technologies.PrincipalRecipeIngredients.md#ConditionalPropertyValue) | string (nullable) | The desired value of Conditional Property in order for the template line to match. 
| [FixedScrapQuantity](Production.Technologies.PrincipalRecipeIngredients.md#FixedScrapQuantity) | [Quantity](../data-types.md#Quantity) | Fixed scrap quantity for setup. [Unit: UsageUnit] [Required] [Default(0)] 
| [IngredientName](Production.Technologies.PrincipalRecipeIngredients.md#IngredientName) | string | The principal name of the ingredient. [Required] [Filter(like)] 
| [LineOrd](Production.Technologies.PrincipalRecipeIngredients.md#LineOrd) | int32 | The position of the line in the recipe model. [Required] 
| [ScrapRate](Production.Technologies.PrincipalRecipeIngredients.md#ScrapRate) | decimal | The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe. [Required] [Default(0)] [Filter(ge;le)] 
| [UsageQuantity](Production.Technologies.PrincipalRecipeIngredients.md#UsageQuantity) | [Quantity](../data-types.md#Quantity) (nullable) | Quantity to be consumed from the material. null means that the quantity is specified with formula. [Unit: UsageUnit] [Default(1)] [Filter(ge;le)] 
| [UsageQuantityFormula](Production.Technologies.PrincipalRecipeIngredients.md#UsageQuantityFormula) | string (nullable) | Specifies formula for the usage quantity. The formula can reference properties in [<Prop_Name>] style, just like products name and description mask. The formula can contain *, /, + and - operators. The formula can also be simple number, directly specifying quantity. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConditionalPropertyAllowedValue](Production.Technologies.PrincipalRecipeIngredients.md#ConditionalPropertyAllowedValue) | [General.CustomPropertyAllowedValues](General.CustomPropertyAllowedValues.md) (nullable) | When not null, specifies that, when creating recipe, the ingredient will be added only if the main product property, specified in Conditional_Property_Id equals the specified value. [Filter(multi eq)] |
| [ConditionalProperty](Production.Technologies.PrincipalRecipeIngredients.md#ConditionalProperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | When not null, specifies that, when creating recipe, the ingredient will be added only if this property is set for the main product. [Filter(multi eq)] |
| [DefaultMaterial](Production.Technologies.PrincipalRecipeIngredients.md#DefaultMaterial) | [General.Products.Products](General.Products.Products.md) (nullable) | If not null, points to default product for this ingredient. [Filter(multi eq)] |
| [DefaultStore](Production.Technologies.PrincipalRecipeIngredients.md#DefaultStore) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The default store from which to retrieve the material. [Filter(multi eq)] |
| [MaterialFromProperty](Production.Technologies.PrincipalRecipeIngredients.md#MaterialFromProperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | When not null, specifies that the material will be obtained from the value of the specified property. The property must have allowed values in the Products domain. [Filter(multi eq)] |
| [MaterialGroup](Production.Technologies.PrincipalRecipeIngredients.md#MaterialGroup) | [General.Products.ProductGroups](General.Products.ProductGroups.md) | Filter for choosing specific material in the recipe (Gen_Product_Groups_Table). [Required] [Filter(multi eq)] |
| [Operation](Production.Technologies.PrincipalRecipeIngredients.md#Operation) | [Production.Resources.Operations](Production.Resources.Operations.md) (nullable) | Specifies for which operation this ingredient will be used. [Filter(multi eq)] |
| [PrincipalRecipe](Production.Technologies.PrincipalRecipeIngredients.md#PrincipalRecipe) | [Production.Technologies.PrincipalRecipes](Production.Technologies.PrincipalRecipes.md) | The [PrincipalRecipe](Production.Technologies.PrincipalRecipeIngredients.md#PrincipalRecipe) to which this PrincipalRecipeIngredient belongs. [Required] [Filter(multi eq)] [Owner] |
| [UsageUnit](Production.Technologies.PrincipalRecipeIngredients.md#UsageUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Usage_Quantity. The selected item must support the specified unit. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConditionalPropertyDescription

> The desired description of Conditional Property in order for the template line to match.

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConditionalPropertyValue

> The desired value of Conditional Property in order for the template line to match.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### FixedScrapQuantity

> Fixed scrap quantity for setup. [Unit: UsageUnit] [Required] [Default(0)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### IngredientName

> The principal name of the ingredient. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DefaultMaterial.Name`
### LineOrd

> The position of the line in the recipe model. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.PrincipalRecipe.Ingredients.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.PrincipalRecipe.Ingredients.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### ScrapRate

> The usual percentage (0..1) of scrap of the raw material; inflates the requirements of this material for this recipe. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **decimal**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### UsageQuantity

> Quantity to be consumed from the material. null means that the quantity is specified with formula. [Unit: UsageUnit] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity) (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`IIF((obj.UsageQuantityFormula != null), null, obj.UsageQuantity)`
### UsageQuantityFormula

> Specifies formula for the usage quantity. The formula can reference properties in [<Prop_Name>] style, just like products name and description mask. The formula can contain *, /, + and - operators. The formula can also be simple number, directly specifying quantity.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.UsageQuantity != null), null, obj.UsageQuantityFormula)`

## Reference Details

### ConditionalPropertyAllowedValue

> When not null, specifies that, when creating recipe, the ingredient will be added only if the main product property, specified in Conditional_Property_Id equals the specified value. [Filter(multi eq)]

_Type_: **[General.CustomPropertyAllowedValues](General.CustomPropertyAllowedValues.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ConditionalProperty

> When not null, specifies that, when creating recipe, the ingredient will be added only if this property is set for the main product. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DefaultMaterial

> If not null, points to default product for this ingredient. [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DefaultStore

> The default store from which to retrieve the material. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MaterialFromProperty

> When not null, specifies that the material will be obtained from the value of the specified property. The property must have allowed values in the Products domain. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MaterialGroup

> Filter for choosing specific material in the recipe (Gen_Product_Groups_Table). [Required] [Filter(multi eq)]

_Type_: **[General.Products.ProductGroups](General.Products.ProductGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Operation

> Specifies for which operation this ingredient will be used. [Filter(multi eq)]

_Type_: **[Production.Resources.Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PrincipalRecipe

> The [PrincipalRecipe](Production.Technologies.PrincipalRecipeIngredients.md#PrincipalRecipe) to which this PrincipalRecipeIngredient belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Technologies.PrincipalRecipes](Production.Technologies.PrincipalRecipes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### UsageUnit

> The measurement unit of Usage_Quantity. The selected item must support the specified unit. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DefaultMaterial.BaseUnit`


## Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipeIngredients erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipeIngredients erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Technologies.PrincipalRecipeIngredients erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_PrincipalRecipeIngredients?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_PrincipalRecipeIngredients?$top=10>

