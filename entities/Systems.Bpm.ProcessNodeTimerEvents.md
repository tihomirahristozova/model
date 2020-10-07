# Systems.Bpm.ProcessNodeTimerEvents

Timer event definition. Currently - not used. Entity: Bpm_Process_Node_Timer_Events

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.ProcessNodeTimerEvents.md#Id) | guid |  
| [ProcessNodeEventId](Systems.Bpm.ProcessNodeTimerEvents.md#ProcessNodeEventId) | guid | The process node event, which this timer defines. [Required] [Filter(multi eq)] 
| [TimeCycle](Systems.Bpm.ProcessNodeTimerEvents.md#TimeCycle) | string (nullable) | Non-null when the timer is recurring. The value conforms to the ISO-8601 format for recurring time intervals. Mutually exclusive with the other Time fields. 
| [TimeDate](Systems.Bpm.ProcessNodeTimerEvents.md#TimeDate) | datetime (nullable) | Non-null when the timer is for specific single date and time. Mutually exclusive with the other Time fields. 
| [TimeDuration](Systems.Bpm.ProcessNodeTimerEvents.md#TimeDuration) | string (nullable) | Non-null when the timer event is for time duration. The value conforms to the ISO-8601 format for time interval representations. Mutually exclusive with the other Time fields. 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ProcessNodeEventId

> The process node event, which this timer defines. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TimeCycle

> Non-null when the timer is recurring. The value conforms to the ISO-8601 format for recurring time intervals. Mutually exclusive with the other Time fields.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TimeDate

> Non-null when the timer is for specific single date and time. Mutually exclusive with the other Time fields.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### TimeDuration

> Non-null when the timer event is for time duration. The value conforms to the ISO-8601 format for time interval representations. Mutually exclusive with the other Time fields.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.ProcessNodeTimerEvents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.ProcessNodeTimerEvents erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.ProcessNodeTimerEvents erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_ProcessNodeTimerEvents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_ProcessNodeTimerEvents?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Bpm_Process_Node_Timer_Events?$top=10>

