---
uid: Systems.Bpm.UserBusinessRuleEvents
---
# Systems.Bpm.UserBusinessRuleEvents Entity

Represents event registration of a business rule. Entity: Sys_User_Business_Rule_Events

Default Display Text Format:  
_{UserBusinessRule.Code}: {UserBusinessRule.RepositoryName:T}_  
Default Search Member:  
_UserBusinessRule.Code_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EventParameter](Systems.Bpm.UserBusinessRuleEvents.md#eventparameter) | string (nullable) | Registration parameter. The meaning is determined by the event. Usually - attribute name, document state, etc. 
| [EventType](Systems.Bpm.UserBusinessRuleEvents.md#eventtype) | [EventType](Systems.Bpm.UserBusinessRuleEvents.md#eventtype) | The event for which to register the business rule. [Required] 
| [ExecutionPriority](Systems.Bpm.UserBusinessRuleEvents.md#executionpriority) | [RuleExecutionPriority](Systems.Bpm.UserBusinessRuleEvents.md#executionpriority) | Execution priority. Lower values indicate earlier priorities. Possible values - 30-Early, 50-Normal, 70-Late. [Required] [Default(50)] 
| [Id](Systems.Bpm.UserBusinessRuleEvents.md#id) | guid |  
| [Layer](Systems.Bpm.UserBusinessRuleEvents.md#layer) | [Layer](Systems.Bpm.UserBusinessRuleEvents.md#layer) | Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd. [Required] [Default("BKE")] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [UserBusinessRule](Systems.Bpm.UserBusinessRuleEvents.md#userbusinessrule) | [UserBusinessRules](Systems.Bpm.UserBusinessRules.md) | The rule, which will be registered for the event. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### EventParameter

Registration parameter. The meaning is determined by the event. Usually - attribute name, document state, etc.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EventType

The event for which to register the business rule. [Required]

_Type_: **[EventType](Systems.Bpm.UserBusinessRuleEvents.md#eventtype)**  
Allowed values for the [EventType](Systems.Bpm.UserBusinessRuleEvents.md#eventtype) data attribute  
_Allowed Values (Systems.Bpm.UserBusinessRuleEventsRepository.EventType Enum Members)_  

| Value | Description |
| ---- | --- |
| AGGREGATECLIENTCOMMIT | Occurs for the aggregate root when saving a change of an aggregate object, but only when the change is made by a client application. If the change is made by the server, the event will not be triggered.. Stored as 'AGGREGATECLIENTCOMMIT'. <br /> _Database Value:_ 'AGGREGATECLIENTCOMMIT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'AGGREGATECLIENTCOMMIT' |
| ATTRIBUTECHANGED | Occurs after the attribute's value is changed. The attribute's name is specified in the 'Event Parameter' field.. Stored as 'ATTRIBUTECHANGED'. <br /> _Database Value:_ 'ATTRIBUTECHANGED' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ATTRIBUTECHANGED' |
| ATTRIBUTECHANGING | Occurs before the attribute's value is changed. The attribute's name is specified in the 'Event Parameter' field.. Stored as 'ATTRIBUTECHANGING'. <br /> _Database Value:_ 'ATTRIBUTECHANGING' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ATTRIBUTECHANGING' |
| CLIENTCOMMIT | Occurs when saving a change of the object, when the change is made by a client application. If the change is made by the server, the event will not be triggered.. Stored as 'CLIENTCOMMIT'. <br /> _Database Value:_ 'CLIENTCOMMIT' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'CLIENTCOMMIT' |
| COMMIT | Occurs when saving a change of the object.. Stored as 'COMMIT'. <br /> _Database Value:_ 'COMMIT' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'COMMIT' |
| STATECHANGED | Occurs when the document state is changed. The state is specified in the 'Event Parameter' field. Possible parameter values are 'PLANNED', 'FIRMPLANNED', 'RELEASED', 'COMPLETED' and 'CLOSED'.. Stored as 'STATECHANGED'. <br /> _Database Value:_ 'STATECHANGED' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'STATECHANGED' |
| STATECHANGING | Occurs during the document state change. The state is specified in the 'Event Parameter' field. Possible parameter values are 'PLANNING', 'FIRMPLANNING', 'RELEASING', 'COMPLETING' and 'CLOSING'.. Stored as 'STATECHANGING'. <br /> _Database Value:_ 'STATECHANGING' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'STATECHANGING' |
| VOIDING | Occurs during the voiding of a document.. Stored as 'VOIDING'. <br /> _Database Value:_ 'VOIDING' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'VOIDING' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ExecutionPriority

Execution priority. Lower values indicate earlier priorities. Possible values - 30-Early, 50-Normal, 70-Late. [Required] [Default(50)]

_Type_: **[RuleExecutionPriority](Systems.Bpm.UserBusinessRuleEvents.md#executionpriority)**  
_Allowed Values (Aloe.SystemFrameworks.Domain.BusinessLogic.RuleExecutionPriority Enum Members)_  

| Value | Description |
| ---- | --- |
| Early | _Database Value:_ 30 <br /> _Model Value:_ 30 <br /> _Domain API Value:_ 'Early' |
| Normal | _Database Value:_ 50 <br /> _Model Value:_ 50 <br /> _Domain API Value:_ 'Normal' |
| Late | _Database Value:_ 70 <br /> _Model Value:_ 70 <br /> _Domain API Value:_ 'Late' |
| SystemLateUpdate | _Database Value:_ 150 <br /> _Model Value:_ 150 <br /> _Domain API Value:_ 'SystemLateUpdate' |
| SystemLateValidate | _Database Value:_ 200 <br /> _Model Value:_ 200 <br /> _Domain API Value:_ 'SystemLateValidate' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **50**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Layer

Specifies the layer on which to register the event. Allowed values = FTE-FrontEnd, BKE-BackEnd. [Required] [Default("BKE")]

_Type_: **[Layer](Systems.Bpm.UserBusinessRuleEvents.md#layer)**  
Allowed values for the [Layer](Systems.Bpm.UserBusinessRuleEvents.md#layer) data attribute  
_Allowed Values (Systems.Bpm.UserBusinessRuleEventsRepository.Layer Enum Members)_  

| Value | Description |
| ---- | --- |
| FrontEnd | FrontEnd value. Stored as 'FTE'. <br /> _Database Value:_ 'FTE' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'FrontEnd' |
| BackEnd | BackEnd value. Stored as 'BKE'. <br /> _Database Value:_ 'BKE' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'BackEnd' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **BackEnd**  


## Reference Details

### UserBusinessRule

The rule, which will be registered for the event. [Required] [Filter(multi eq)] [Owner]

_Type_: **[UserBusinessRules](Systems.Bpm.UserBusinessRules.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Bpm.UserBusinessRuleEvents erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.UserBusinessRuleEvents erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_UserBusinessRuleEvents?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_UserBusinessRuleEvents?$top=10>

