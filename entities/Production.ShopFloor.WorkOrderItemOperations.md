---
uid: Production.ShopFloor.WorkOrderItemOperations
---
# Production.ShopFloor.WorkOrderItemOperations

The operations that are performed to produce the product. Entity: Prd_Work_Order_Item_Operations

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.ShopFloor.WorkOrderItemOperations.md#Id) | guid |  
| [ActualEndDateTime](Production.ShopFloor.WorkOrderItemOperations.md#ActualEndDateTime) | datetime (nullable) | The date/time when the operation has completed. null means that the operation is not completed. 
| [ActualStartDateTime](Production.ShopFloor.WorkOrderItemOperations.md#ActualStartDateTime) | datetime (nullable) | The date/time when the operation has started. null means that the has not started yet. 
| [LineOrd](Production.ShopFloor.WorkOrderItemOperations.md#LineOrd) | int32 | Order of the line within the work order routing. [Required] [Filter(eq;like)] 
| [MinimumConcurrentStartTimeMinutes](Production.ShopFloor.WorkOrderItemOperations.md#MinimumConcurrentStartTimeMinutes) | int32 (nullable) | How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting. 
| [MoveTimeMinutes](Production.ShopFloor.WorkOrderItemOperations.md#MoveTimeMinutes) | int32 | Time to move the lot to the next operation in minutes. [Required] [Default(0)] 
| [Notes](Production.ShopFloor.WorkOrderItemOperations.md#Notes) | string (nullable) | Notes for this WorkOrderItemOperation. 
| [OperationDescription](Production.ShopFloor.WorkOrderItemOperations.md#OperationDescription) | string (nullable) | The short description of the operation. 
| [RunTimeMinutes](Production.ShopFloor.WorkOrderItemOperations.md#RunTimeMinutes) | int32 | Time for production of one lot of the produced item in minutes. [Required] [Default(0)] 
| [ScheduledEndDateTime](Production.ShopFloor.WorkOrderItemOperations.md#ScheduledEndDateTime) | datetime (nullable) | The date/time when the operation is scheduled to complete. null means that there is still no plan when the operation will finish (for new orders only). 
| [ScheduledStartDateTime](Production.ShopFloor.WorkOrderItemOperations.md#ScheduledStartDateTime) | datetime (nullable) | The date/time when the operation is planned to start. null means that there is still no plan when to start the operaion (only for new work orders). 
| [ScrapRate](Production.ShopFloor.WorkOrderItemOperations.md#ScrapRate) | decimal | Projected scrap rate of the operation. [Required] [Default(0)] 
| [SetupTimeMinutes](Production.ShopFloor.WorkOrderItemOperations.md#SetupTimeMinutes) | int32 | Time needed to setup the equipment in minutes. [Required] [Default(0)] 
| [Tooling](Production.ShopFloor.WorkOrderItemOperations.md#Tooling) | string (nullable) | The tools needed for the routing step. 
| [UseQuantity](Production.ShopFloor.WorkOrderItemOperations.md#UseQuantity) | [Quantity](../data-types.md#Quantity) | Quantity of the resource, that should be allocated for the operation. [Unit: WorkgroupResource.Resource.PrimaryUnit] [Required] [Default(1)] 
| [WaitTimeMinutes](Production.ShopFloor.WorkOrderItemOperations.md#WaitTimeMinutes) | int32 | Wait time (drying, cooling, etc.) after the operation in minutes. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Operation](Production.ShopFloor.WorkOrderItemOperations.md#Operation) | [Production.Resources.Operations](Production.Resources.Operations.md) (nullable) | The performed operation. [Filter(multi eq)] |
| [WorkOrderItem](Production.ShopFloor.WorkOrderItemOperations.md#WorkOrderItem) | [Production.ShopFloor.WorkOrderItems](Production.ShopFloor.WorkOrderItems.md) | The work order item, containing the line. [Required] [Filter(multi eq)] [Owner] |
| [WorkgroupResource](Production.ShopFloor.WorkOrderItemOperations.md#WorkgroupResource) | [Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md) | The resource that will be used for the operation. null means that no resource will be locked for the operation. [Required] [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Load | [Production.Resources.Load](Production.Resources.Load.md) | List of [Load](Production.Resources.Load.md) child objects, based on the [Production.Resources.Load.WorkOrderItemOperation](Production.Resources.Load.md#WorkOrderItemOperation) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ActualEndDateTime

> The date/time when the operation has completed. null means that the operation is not completed.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ActualStartDateTime

> The date/time when the operation has started. null means that the has not started yet.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineOrd

> Order of the line within the work order routing. [Required] [Filter(eq;like)]

_Type_: **int32**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.WorkOrderItem.Operations.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.WorkOrderItem.Operations.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
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

> Notes for this WorkOrderItemOperation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### OperationDescription

> The short description of the operation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.Operation.Name`
### RunTimeMinutes

> Time for production of one lot of the produced item in minutes. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ScheduledEndDateTime

> The date/time when the operation is scheduled to complete. null means that there is still no plan when the operation will finish (for new orders only).

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScheduledStartDateTime

> The date/time when the operation is planned to start. null means that there is still no plan when to start the operaion (only for new work orders).

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScrapRate

> Projected scrap rate of the operation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### SetupTimeMinutes

> Time needed to setup the equipment in minutes. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Tooling

> The tools needed for the routing step.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UseQuantity

> Quantity of the resource, that should be allocated for the operation. [Unit: WorkgroupResource.Resource.PrimaryUnit] [Required] [Default(1)]

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

> The performed operation. [Filter(multi eq)]

_Type_: **[Production.Resources.Operations](Production.Resources.Operations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WorkOrderItem

> The work order item, containing the line. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.ShopFloor.WorkOrderItems](Production.ShopFloor.WorkOrderItems.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WorkgroupResource

> The resource that will be used for the operation. null means that no resource will be locked for the operation. [Required] [Filter(multi eq)]

_Type_: **[Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrderItemOperations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.ShopFloor.WorkOrderItemOperations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.ShopFloor.WorkOrderItemOperations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_ShopFloor_WorkOrderItemOperations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_ShopFloor_WorkOrderItemOperations?$top=10>

