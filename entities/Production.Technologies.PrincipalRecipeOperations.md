---
uid: Production.Technologies.PrincipalRecipeOperations
---
# Production.Technologies.PrincipalRecipeOperations Entity

**Namespace:** [Production.Technologies](Production.Technologies.md)  

Contains the operations within a principal recipe. Entity: Prd_Principal_Recipe_Operations

## Default Visualization
Default Display Text Format:  
_{PrincipalRecipe.Name:T}_  
Default Search Member:  
_PrincipalRecipe.Name_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[Production.Technologies.PrincipalRecipes](Production.Technologies.PrincipalRecipes.md)  
Aggregate Root:  
[General.Products.ProductGroups](General.Products.ProductGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConditionalProperty<br />Description](Production.Technologies.PrincipalRecipeOperations.md#conditionalpropertydescription) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | The desired description of the Conditional Property. . 
| [ConditionalPropertyValue](Production.Technologies.PrincipalRecipeOperations.md#conditionalpropertyvalue) | string (nullable) | The desired value of the Conditional Property. . 
| [Id](Production.Technologies.PrincipalRecipeOperations.md#id) | guid |  
| [LineOrd](Production.Technologies.PrincipalRecipeOperations.md#lineord) | int32 | Consecutive line number within the principal recipe. [Required] 
| [MinimumConcurrent<br />StartTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#minimumconcurrentstarttimeminutes) | int32 (nullable) | How many minutes after the start of the previous operation can this operation start. null means that this operation should wait the previous operation to finish before starting. 
| [MoveTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#movetimeminutes) | int32 | Time to move the lot to the next operation in minutes. [Required] [Default(0)] [Filter(ge;le)] 
| [Notes](Production.Technologies.PrincipalRecipeOperations.md#notes) | string (nullable) | Notes for this PrincipalRecipeOperation. 
| [OperationDescription](Production.Technologies.PrincipalRecipeOperations.md#operationdescription) | string (nullable) | The description of the operation. Initially copied from the generic operation definition. 
| [RunTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#runtimeminutes) | int32 | Duration of the operation for one piece in the standard measurement unit of the product. [Required] [Default(0)] [Filter(ge;le)] 
| [ScrapRate](Production.Technologies.PrincipalRecipeOperations.md#scraprate) | decimal | Standard rate of scrap during the operation. [Required] [Default(0)] 
| [SetupTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#setuptimeminutes) | int32 | Time needed to setup the equipment. [Required] [Default(0)] [Filter(ge;le)] 
| [Tooling](Production.Technologies.PrincipalRecipeOperations.md#tooling) | string (nullable) | The tools needed for the routing step. 
| [UseQuantity](Production.Technologies.PrincipalRecipeOperations.md#usequantity) | [Quantity](../data-types.md#quantity) | Quantity of the workgroup resource that should be allocated for the operation. [Unit: UseQuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [WaitTimeMinutes](Production.Technologies.PrincipalRecipeOperations.md#waittimeminutes) | int32 | Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConditionalProperty](Production.Technologies.PrincipalRecipeOperations.md#conditionalproperty) | [CustomProperties](General.CustomProperties.md) (nullable) | When not null, specifies that, when creating recipe, the operation will be added only if this property is set for the main product. [Filter(multi eq)] |
| [Operation](Production.Technologies.PrincipalRecipeOperations.md#operation) | [Operations](Production.Resources.Operations.md) (nullable) | The generic operation definition. The data is copied locally and can be modified for this specific record. [Filter(multi eq)] |
| [OperationInstruction](Production.Technologies.PrincipalRecipeOperations.md#operationinstruction) | [OperationInstructions](Production.Resources.OperationInstructions.md) (nullable) | Link to additional data, containing instructions in external format. [Filter(multi eq)] |
| [PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#principalrecipe) | [PrincipalRecipes](Production.Technologies.PrincipalRecipes.md) | The [PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#principalrecipe) to which this PrincipalRecipeOperation belongs. [Required] [Filter(multi eq)] [Owner] |
| [UseQuantityUnit](Production.Technologies.PrincipalRecipeOperations.md#usequantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Use_Quantity. [Required] [Filter(multi eq)] |
| [WorkgroupResource](Production.Technologies.PrincipalRecipeOperations.md#workgroupresource) | [WorkgroupResources](Production.Resources.WorkgroupResources.md) | Required workgroup resource for the operation. null means that no resource is required or the resource will be specified later. [Required] [Filter(multi eq)] |


## Attribute Details

### ConditionalPropertyDescription

The desired description of the Conditional Property. .

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConditionalPropertyValue

The desired value of the Conditional Property. .

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineOrd

Consecutive line number within the principal recipe. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.PrincipalRecipe.Operations.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.PrincipalRecipe.Operations.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`
### MinimumConcurrentStartTimeMinutes

How many minutes after the start of the previous operation can this operation start. null means that this operation should wait the previous operation to finish before starting.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MoveTimeMinutes

Time to move the lot to the next operation in minutes. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.MoveTimeMinutes`
### Notes

Notes for this PrincipalRecipeOperation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OperationDescription

The description of the operation. Initially copied from the generic operation definition.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Operation.Description`
### RunTimeMinutes

Duration of the operation for one piece in the standard measurement unit of the product. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.RunTimeMinutes`
### ScrapRate

Standard rate of scrap during the operation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### SetupTimeMinutes

Time needed to setup the equipment. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.SetupTimeMinutes`
### Tooling

The tools needed for the routing step.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UseQuantity

Quantity of the workgroup resource that should be allocated for the operation. [Unit: UseQuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.Operation.UseQuantityBase`
### WaitTimeMinutes

Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

_Front-End Recalc Expressions:_  
`obj.Operation.WaitTimeMinutes`

## Reference Details

### ConditionalProperty

When not null, specifies that, when creating recipe, the operation will be added only if this property is set for the main product. [Filter(multi eq)]

_Type_: **[CustomProperties](General.CustomProperties.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Operation

The generic operation definition. The data is copied locally and can be modified for this specific record. [Filter(multi eq)]

_Type_: **[Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### OperationInstruction

Link to additional data, containing instructions in external format. [Filter(multi eq)]

_Type_: **[OperationInstructions](Production.Resources.OperationInstructions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PrincipalRecipe

The [PrincipalRecipe](Production.Technologies.PrincipalRecipeOperations.md#principalrecipe) to which this PrincipalRecipeOperation belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[PrincipalRecipes](Production.Technologies.PrincipalRecipes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### UseQuantityUnit

The measurement unit of Use_Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( obj.WorkgroupResource.Resource != null), obj.WorkgroupResource.Resource.PrimaryUnit, obj.UseQuantityUnit)`
### WorkgroupResource

Required workgroup resource for the operation. null means that no resource is required or the resource will be specified later. [Required] [Filter(multi eq)]

_Type_: **[WorkgroupResources](Production.Resources.WorkgroupResources.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Operation.WorkgroupResource`


## Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipeOperations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Technologies.PrincipalRecipeOperations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Technologies_PrincipalRecipeOperations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Technologies_PrincipalRecipeOperations?$top=10>

