# Production.Resources.Load

Contains scheduled operations usage of the resources. Entity: Prd_Load

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Production.Resources.Load.md#Id) | guid |  
| [CalendarDate](Production.Resources.Load.md#CalendarDate) | datetime | Date of the scheduled load. This is date only. Start_Time and End_Time specify time of day. [Required] [Filter(ge;le)] 
| [Priority](Production.Resources.Load.md#Priority) | [Production.Resources.LoadRepository.Priority](Production.Resources.Load.md#Priority) | Priority of the allocation. 1=Lowest ... 5=Highest. [Required] [Default(3)] 
| [TimeType](Production.Resources.Load.md#TimeType) | [Production.Resources.LoadRepository.TimeType](Production.Resources.Load.md#TimeType) | S=Setup; R=Run; W=Wait; M=Move. [Required] [Default("R")] 
| [UsageEndTime](Production.Resources.Load.md#UsageEndTime) | datetime | The ending time of the planned usage. [Required] [Filter(ge;le)] 
| [UsageQuantity](Production.Resources.Load.md#UsageQuantity) | [Quantity](../data-types/Quantity.md) | Quantity of the resource, which will be used for production. [Unit: WorkgroupResource.Resource.PrimaryUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [UsageStartTime](Production.Resources.Load.md#UsageStartTime) | datetime | The starting time of the planned usage. [Required] [Filter(ge;le)] 
| [UsageTimeMinutes](Production.Resources.Load.md#UsageTimeMinutes) | int32 | Time allocated for the operation in minutes. [Required] [Default(0)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [WorkOrderItemOperation](Production.Resources.Load.md#WorkOrderItemOperation) | [Production.ShopFloor.WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md) | The [WorkOrderItemOperation](Production.ShopFloor.WorkOrderItemOperations.md) to which this Load belongs. [Required] [Filter(multi eq)] [Owner] |
| [WorkgroupResource](Production.Resources.Load.md#WorkgroupResource) | [Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md) | The exact resource being utilised. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CalendarDate

> Date of the scheduled load. This is date only. Start_Time and End_Time specify time of day. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Priority

> Priority of the allocation. 1=Lowest ... 5=Highest. [Required] [Default(3)]

_Type_: **[Production.Resources.LoadRepository.Priority](Production.Resources.Load.md#Priority)**  
Allowed values for the [Priority](Production.Resources.Load.md#Priority) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Lowest | Lowest value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Lowest' |
| Two | Two value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Two' |
| Three | Three value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Three' |
| Four | Four value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Four' |
| Highest | Highest value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Highest' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **3**  

### TimeType

> S=Setup; R=Run; W=Wait; M=Move. [Required] [Default("R")]

_Type_: **[Production.Resources.LoadRepository.TimeType](Production.Resources.Load.md#TimeType)**  
Allowed values for the [TimeType](Production.Resources.Load.md#TimeType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Move | Move value. Stored as 'M'. <br /> _Database Value:_ 'M' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Move' |
| Run | Run value. Stored as 'R'. <br /> _Database Value:_ 'R' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Run' |
| Setup | Setup value. Stored as 'S'. <br /> _Database Value:_ 'S' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Setup' |
| Wait | Wait value. Stored as 'W'. <br /> _Database Value:_ 'W' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Wait' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Run**  

### UsageEndTime

> The ending time of the planned usage. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UsageQuantity

> Quantity of the resource, which will be used for production. [Unit: WorkgroupResource.Resource.PrimaryUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types/Quantity.md)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### UsageStartTime

> The starting time of the planned usage. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### UsageTimeMinutes

> Time allocated for the operation in minutes. [Required] [Default(0)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### WorkOrderItemOperation

> The [WorkOrderItemOperation](Production.ShopFloor.WorkOrderItemOperations.md) to which this Load belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Production.ShopFloor.WorkOrderItemOperations](Production.ShopFloor.WorkOrderItemOperations.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WorkgroupResource

> The exact resource being utilised. [Required] [Filter(multi eq)]

_Type_: **[Production.Resources.WorkgroupResources](Production.Resources.WorkgroupResources.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Production.Resources.Load erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Production.Resources.Load erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Production.Resources.Load erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Production_Resources_Load?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Production_Resources_Load?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Prd_Load?$top=10>

