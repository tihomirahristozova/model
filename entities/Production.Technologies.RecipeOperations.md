---
uid: Production.Technologies.RecipeOperations
---
# Production.Technologies.RecipeOperations

Contains the routing (operation list) of the recipes. Entity: Prd_Recipe_Operations

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Technologies.RecipeOperations.md#Id) | guid |  
| [LineOrd](Production.Technologies.RecipeOperations.md#LineOrd) | int32 | Order of the operation within the recipe. [Required] 
| [MinimumConcurrentStartTimeMinutes](Production.Technologies.RecipeOperations.md#MinimumConcurrentStartTimeMinutes) | int32 (nullable) | How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting. 
| [MoveTimeMinutes](Production.Technologies.RecipeOperations.md#MoveTimeMinutes) | int32 | Time to move the lot to the next operation in minutes. [Required] [Default(0)] 
| [Notes](Production.Technologies.RecipeOperations.md#Notes) | string (nullable) | Notes for this RecipeOperation. 
| [OperationDescription](Production.Technologies.RecipeOperations.md#OperationDescription) | string (nullable) | The description of the operation. 
| [RunTimeMinutes](Production.Technologies.RecipeOperations.md#RunTimeMinutes) | int32 | Duration of the operation for standard lot of the product. [Required] [Default(0)] 
| [ScrapRate](Production.Technologies.RecipeOperations.md#ScrapRate) | decimal | Standard rate of scrap during the operation. [Required] [Default(0)] 
| [SetupTimeMinutes](Production.Technologies.RecipeOperations.md#SetupTimeMinutes) | int32 | Time needed to setup the equipment. [Required] [Default(0)] 
| [StandardCostPerHour](Production.Technologies.RecipeOperations.md#StandardCostPerHour) | [Amount](../data-types.md#Amount) (nullable) | Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe. [Currency: Recipe.Product.CostingCurrency] 
| [StandardPricePerHour](Production.Technologies.RecipeOperations.md#StandardPricePerHour) | [Amount](../data-types.md#Amount) | Standard price for 1 hour work. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)] 
| [Tooling](Production.Technologies.RecipeOperations.md#Tooling) | string (nullable) | The tools needed for the routing step. 
| [UseQuantity](Production.Technologies.RecipeOperations.md#UseQuantity) | [Quantity](../data-types.md#Quantity) | Quantity of the workgroup resource that should be allocated for the operation. [Unit: UseQuantityUnit] [Required] [Default(1)] 
| [WaitTimeMinutes](Production.Technologies.RecipeOperations.md#WaitTimeMinutes) | int32 | Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Operation](Production.Technologies.RecipeOperations.md#Operation) | [Production.Resources.Operations](Production.Resources.Operations.md) (nullable) | Standard operation Id. If not null used to load the details. If null the details (times, scrap rates, etc.) must be entered manually. [Filter(multi eq)] |
| [OperationInstruction](Production.Technologies.RecipeOperations.md#OperationInstruction) | [Production.Resources.OperationInstructions](Production.Resources.OperationInstructions.md) (nullable) | Link to additional data, containing instructions in external format. [Filter(multi eq)] |
| [Recipe](Production.Technologies.RecipeOperations.md#Recipe) | [Production.Technologies.Recipes](Production.Technologies.Recipes.md) | The [Recipe](Production.Technologies.RecipeOperations.md#Recipe) to which this RecipeOperation belongs. [Required] [Filter(multi eq)] [Owner] |
| [UseQuantityUnit](Production.Technologies.RecipeOperations.md#UseQuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Use_Quantity. [Required] [Filter(multi eq)] |
| [WorkgroupResource](Production.Technologies.RecipeOperations.md#WorkgroupResource) | [Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md) | The exact workgroup resource that is engaged in the operation. null means that no resource is needed or it will be specfied at a later stage. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### LineOrd

> Order of the operation within the recipe. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.Recipe.Operations.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.Recipe.Operations.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### MinimumConcurrentStartTimeMinutes

> How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MoveTimeMinutes

> Time to move the lot to the next operation in minutes. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Notes

> Notes for this RecipeOperation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OperationDescription

> The description of the operation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RunTimeMinutes

> Duration of the operation for standard lot of the product. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ScrapRate

> Standard rate of scrap during the operation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### SetupTimeMinutes

> Time needed to setup the equipment. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StandardCostPerHour

> Standard cost per hour for this operation. It participates in the calculation of standard cost for production for the whole recipe. [Currency: Recipe.Product.CostingCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StandardPricePerHour

> Standard price for 1 hour work. [Currency: Recipe.Product.CostingCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Tooling

> The tools needed for the routing step.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UseQuantity

> Quantity of the workgroup resource that should be allocated for the operation. [Unit: UseQuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### WaitTimeMinutes

> Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Operation

> Standard operation Id. If not null used to load the details. If null the details (times, scrap rates, etc.) must be entered manually. [Filter(multi eq)]

_Type_: **[Production.Resources.Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OperationInstruction

> Link to additional data, containing instructions in external format. [Filter(multi eq)]

_Type_: **[Production.Resources.OperationInstructions](Production.Resources.OperationInstructions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Recipe

> The [Recipe](Production.Technologies.RecipeOperations.md#Recipe) to which this RecipeOperation belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Technologies.Recipes](Production.Technologies.Recipes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### UseQuantityUnit

> The measurement unit of Use_Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WorkgroupResource

> The exact workgroup resource that is engaged in the operation. null means that no resource is needed or it will be specfied at a later stage. [Required] [Filter(multi eq)]

_Type_: **[Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Technologies.RecipeOperations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Technologies.RecipeOperations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Technologies.RecipeOperations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_RecipeOperations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_RecipeOperations?$top=10>

