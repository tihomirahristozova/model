---
uid: Production.Resources.Operations
---
# Production.Resources.Operations Entity

The different steps performed to create products. Entity: Prd_Operations

Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](Production.Resources.Operations.md#description) | string (nullable) | The description of this Operation. 
| [Id](Production.Resources.Operations.md#id) | guid |  
| [MinimumConcurrent<br />StartTimeMinutes](Production.Resources.Operations.md#minimumconcurrentstarttimeminutes) | int32 (nullable) | How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting. 
| [MoveTimeMinutes](Production.Resources.Operations.md#movetimeminutes) | int32 | The time required for the product to move to the next operation. During this time no resource is allocated. [Required] [Default(0)] 
| [Name](Production.Resources.Operations.md#name) | string | The name of this Operation. [Required] [Filter(like)] 
| [RunTimeMinutes](Production.Resources.Operations.md#runtimeminutes) | int32 | The time required to process one product lot. The run time is calculated for each produced lot. [Required] [Default(0)] 
| [ScrapRate](Production.Resources.Operations.md#scraprate) | decimal (nullable) | The percentage (0..1) of scrap usually occurring during the production operation. null means that the scrap rate cannot be generally calculated. 
| [SetupTimeMinutes](Production.Resources.Operations.md#setuptimeminutes) | int32 | The time required to setup the operation. The setup is incurred only once, regardless of the produced quntity. [Required] [Default(0)] 
| [StandardPricePerHour](Production.Resources.Operations.md#standardpriceperhour) | decimal | Standard price for 1 hour work for this operation. [Required] [Default(0)] 
| [Tooling](Production.Resources.Operations.md#tooling) | string (nullable) | Short description of the needed instruments for the operation. 
| [UseQuantityBase](Production.Resources.Operations.md#usequantitybase) | [Quantity](../data-types.md#quantity) | Quantity of the resource that need to be allocated for the operation, in base measurement units for the resource. [Unit: WorkgroupResource.Resource.PrimaryUnit] [Required] [Default(1)] 
| [WaitTimeMinutes](Production.Resources.Operations.md#waittimeminutes) | int32 | The time required to wait after completing the operation. During this time, the resource is still allocated to the operation. [Required] [Default(0)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [OperationGroup](Production.Resources.Operations.md#operationgroup) | [OperationGroups](Production.Resources.OperationGroups.md) | The [OperationGroup](Production.Resources.Operations.md#operationgroup) to which this Operation belongs. [Required] [Filter(multi eq)] [Owner] |
| [OperationInstructions](Production.Resources.Operations.md#operationinstructions) | [OperationInstructions](Production.Resources.OperationInstructions.md) (nullable) | Full instructions for the operation. [Filter(multi eq)] |
| [WorkgroupResource](Production.Resources.Operations.md#workgroupresource) | [WorkgroupResources](Production.Resources.WorkgroupResources.md) (nullable) | When not null, specifies the Workgroup Resource, which is required by the operation. [Filter(multi eq)] |


## Attribute Details

### Description

The description of this Operation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### MinimumConcurrentStartTimeMinutes

How many minutes after the start of this operation can the next operation start. null means that the next operation should wait this operation to finish before starting.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### MoveTimeMinutes

The time required for the product to move to the next operation. During this time no resource is allocated. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Name

The name of this Operation. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RunTimeMinutes

The time required to process one product lot. The run time is calculated for each produced lot. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### ScrapRate

The percentage (0..1) of scrap usually occurring during the production operation. null means that the scrap rate cannot be generally calculated.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SetupTimeMinutes

The time required to setup the operation. The setup is incurred only once, regardless of the produced quntity. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### StandardPricePerHour

Standard price for 1 hour work for this operation. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Tooling

Short description of the needed instruments for the operation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UseQuantityBase

Quantity of the resource that need to be allocated for the operation, in base measurement units for the resource. [Unit: WorkgroupResource.Resource.PrimaryUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### WaitTimeMinutes

The time required to wait after completing the operation. During this time, the resource is still allocated to the operation. [Required] [Default(0)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### OperationGroup

The [OperationGroup](Production.Resources.Operations.md#operationgroup) to which this Operation belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[OperationGroups](Production.Resources.OperationGroups.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### OperationInstructions

Full instructions for the operation. [Filter(multi eq)]

_Type_: **[OperationInstructions](Production.Resources.OperationInstructions.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WorkgroupResource

When not null, specifies the Workgroup Resource, which is required by the operation. [Filter(multi eq)]

_Type_: **[WorkgroupResources](Production.Resources.WorkgroupResources.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Production.Resources.Operations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.Operations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Operations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Operations?$top=10>

