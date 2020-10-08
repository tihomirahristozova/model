---
uid: Production.Technologies.PrincipalRecipeOperations
---
# Production.Technologies.PrincipalRecipeOperations

Contains the operations within a principal recipe. Entity: Prd_Principal_Recipe_Operations

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Technologies.PrincipalRecipeOperations.md#Id) | guid |  
| [ConditionalPropertyDescription](Production.Technologies.PrincipalRecipeOperations.md#ConditionalPropertyDescription) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The desired description of the Conditional Property. . 
| [ConditionalPropertyValue](Production.Technologies.PrincipalRecipeOperations.md#ConditionalPropertyValue) | string (nullable) | The desired value of the Conditional Property. . 
| [LineOrd](Production.Technologies.PrincipalRecipeOperations.md#LineOrd) | int32 | Consecutive line number within the principal recipe. [Required] 
| [MinimumConcurrentStartTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#MinimumConcurrentStartTimeMinutes) | int32 (nullable) | How many minutes after the start of the previous operation can this operation start. null means that this operation should wait the previous operation to finish before starting. 
| [MoveTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#MoveTimeMinutes) | int32 | Time to move the lot to the next operation in minutes. [Required] [Default(0)] [Filter(ge;le)] 
| [Notes](Production.Technologies.PrincipalRecipeOperations.md#Notes) | string (nullable) | Notes for this PrincipalRecipeOperation. 
| [OperationDescription](Production.Technologies.PrincipalRecipeOperations.md#OperationDescription) | string (nullable) | The description of the operation. Initially copied from the generic operation definition. 
| [RunTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#RunTimeMinutes) | int32 | Duration of the operation for one piece in the standard measurement unit of the product. [Required] [Default(0)] [Filter(ge;le)] 
| [ScrapRate](Production.Technologies.PrincipalRecipeOperations.md#ScrapRate) | decimal | Standard rate of scrap during the operation. [Required] [Default(0)] 
| [SetupTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#SetupTimeMinutes) | int32 | Time needed to setup the equipment. [Required] [Default(0)] [Filter(ge;le)] 
| [Tooling](Production.Technologies.PrincipalRecipeOperations.md#Tooling) | string (nullable) | The tools needed for the routing step. 
| [UseQuantity](Production.Technologies.PrincipalRecipeOperations.md#UseQuantity) | [Quantity](../data-types.md#Quantity) | Quantity of the workgroup resource that should be allocated for the operation. [Unit: UseQuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [WaitTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#WaitTimeMinutes) | int32 | Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConditionalProperty](Production.Technologies.PrincipalRecipeOperations.md#ConditionalProperty) | [General.CustomProperties](General.CustomProperties.md) (nullable) | When not null, specifies that, when creating recipe, the operation will be added only if this property is set for the main product. [Filter(multi eq)] |
| [Operation](Production.Technologies.PrincipalRecipeOperations.md#Operation) | [Production.Resources.Operations](Production.Resources.Operations.md) (nullable) | The generic operation definition. The data is copied locally and can be modified for this specific record. [Filter(multi eq)] |
| [OperationInstruction](Production.Technologies.PrincipalRecipeOperations.md#OperationInstruction) | [Production.Resources.OperationInstructions](Production.Resources.OperationInstructions.md) (nullable) | Link to additional data, containing instructions in external format. [Filter(multi eq)] |
| [PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#PrincipalRecipe) | [Production.Technologies.PrincipalRecipes](Production.Technologies.PrincipalRecipes.md) | The [PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#PrincipalRecipe) to which this PrincipalRecipeOperation belongs. [Required] [Filter(multi eq)] [Owner] |
| [UseQuantityUnit](Production.Technologies.PrincipalRecipeOperations.md#UseQuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Use_Quantity. [Required] [Filter(multi eq)] |
| [WorkgroupResource](Production.Technologies.PrincipalRecipeOperations.md#WorkgroupResource) | [Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md) | Required workgroup resource for the operation. null means that no resource is required or the resource will be specified later. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConditionalPropertyDescription

> The desired description of the Conditional Property. .

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConditionalPropertyValue

> The desired value of the Conditional Property. .

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineOrd

> Consecutive line number within the principal recipe. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.PrincipalRecipe.Operations.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.PrincipalRecipe.Operations.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### MinimumConcurrentStartTimeMinutes

> How many minutes after the start of the previous operation can this operation start. null means that this operation should wait the previous operation to finish before starting.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MoveTimeMinutes

> Time to move the lot to the next operation in minutes. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.MoveTimeMinutes`
### Notes

> Notes for this PrincipalRecipeOperation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OperationDescription

> The description of the operation. Initially copied from the generic operation definition.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Operation.Description`
### RunTimeMinutes

> Duration of the operation for one piece in the standard measurement unit of the product. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.RunTimeMinutes`
### ScrapRate

> Standard rate of scrap during the operation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### SetupTimeMinutes

> Time needed to setup the equipment. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.SetupTimeMinutes`
### Tooling

> The tools needed for the routing step.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UseQuantity

> Quantity of the workgroup resource that should be allocated for the operation. [Unit: UseQuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.Operation.UseQuantityBase`
### WaitTimeMinutes

> Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.WaitTimeMinutes`

## Reference Details

### ConditionalProperty

> When not null, specifies that, when creating recipe, the operation will be added only if this property is set for the main product. [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Operation

> The generic operation definition. The data is copied locally and can be modified for this specific record. [Filter(multi eq)]

_Type_: **[Production.Resources.Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### OperationInstruction

> Link to additional data, containing instructions in external format. [Filter(multi eq)]

_Type_: **[Production.Resources.OperationInstructions](Production.Resources.OperationInstructions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PrincipalRecipe

> The [PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#PrincipalRecipe) to which this PrincipalRecipeOperation belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.Technologies.PrincipalRecipes](Production.Technologies.PrincipalRecipes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### UseQuantityUnit

> The measurement unit of Use_Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((obj.WorkgroupResource.Resource != null), obj.WorkgroupResource.Resource.PrimaryUnit, obj.UseQuantityUnit)`
### WorkgroupResource

> Required workgroup resource for the operation. null means that no resource is required or the resource will be specified later. [Required] [Filter(multi eq)]

_Type_: **[Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Operation.WorkgroupResource`


## Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipeOperations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipeOperations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Technologies.PrincipalRecipeOperations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_PrincipalRecipeOperations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_PrincipalRecipeOperations?$top=10>

