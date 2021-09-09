---
uid: Systems.Bpm.UserBusinessRuleActions
---
# Systems.Bpm.UserBusinessRuleActions Entity

**Namespace:** [Systems.Bpm](Systems.Bpm.md)  

Represents an action within a business rule. Entity: Sys_User_Business_Rule_Actions

## Default Visualization
Default Display Text Format:  
_{UserBusinessRule.RepositoryName:T} : {UserBusinessRule.Code}_  
Default Search Member:  
_UserBusinessRule.RepositoryName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Bpm.UserBusinessRules](Systems.Bpm.UserBusinessRules.md)  
Aggregate Root:  
[Systems.Bpm.UserBusinessRules](Systems.Bpm.UserBusinessRules.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ActionNo](Systems.Bpm.UserBusinessRuleActions.md#actionno) | int32 | Consecutive number of the action, unique within the business rule. `Required` 
| [ActionType](Systems.Bpm.UserBusinessRuleActions.md#actiontype) | [ActionType](Systems.Bpm.UserBusinessRuleActions.md#actiontype) | Specifies the type of action to perform. `Required` 
| [Id](Systems.Bpm.UserBusinessRuleActions.md#id) | guid |  
| [Parameter1Type](Systems.Bpm.UserBusinessRuleActions.md#parameter1type) | [ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#parameter1type) __nullable__ | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter1Value](Systems.Bpm.UserBusinessRuleActions.md#parameter1value) | string (256) __nullable__ | The actual value of the parameter. 
| [Parameter2Type](Systems.Bpm.UserBusinessRuleActions.md#parameter2type) | [ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#parameter2type) __nullable__ | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter2Value](Systems.Bpm.UserBusinessRuleActions.md#parameter2value) | string (256) __nullable__ | The actual value of the parameter. 
| [Parameter3Type](Systems.Bpm.UserBusinessRuleActions.md#parameter3type) | [ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#parameter3type) __nullable__ | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter3Value](Systems.Bpm.UserBusinessRuleActions.md#parameter3value) | string (256) __nullable__ | The actual value of the parameter. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [UserBusinessRule](Systems.Bpm.UserBusinessRuleActions.md#userbusinessrule) | [UserBusinessRules](Systems.Bpm.UserBusinessRules.md) | The business rule, for which the action is defined. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ActionNo

Consecutive number of the action, unique within the business rule. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.UserBusinessRule.Actions.Select( c => c.ActionNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.UserBusinessRule.Actions.Select( c => c.ActionNo).DefaultIfEmpty( 0).Max( ) + 10)`
### ActionType

Specifies the type of action to perform. `Required`

_Type_: **[ActionType](Systems.Bpm.UserBusinessRuleActions.md#actiontype)**  
Allowed values for the `ActionType`(Systems.Bpm.UserBusinessRuleActions.md#actiontype) data attribute  
_Allowed Values (Systems.Bpm.UserBusinessRuleActionsRepository.ActionType Enum Members)_  

| Value | Description |
| ---- | --- |
| SETVALUE | SETVALUE value. Stored as 'SETVALUE'. <br /> _Database Value:_ 'SETVALUE' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SETVALUE' |
| FAIL | FAIL value. Stored as 'FAIL'. <br /> _Database Value:_ 'FAIL' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FAIL' |
| SENDMAIL | SENDMAIL value. Stored as 'SENDMAIL'. <br /> _Database Value:_ 'SENDMAIL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'SENDMAIL' |
| WARNING | WARNING value. Stored as 'WARNING'. <br /> _Database Value:_ 'WARNING' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'WARNING' |
| NOTIFYUSER | NOTIFYUSER value. Stored as 'NOTIFYUSER'. <br /> _Database Value:_ 'NOTIFYUSER' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'NOTIFYUSER' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Parameter1Type

The type of the parameter specifies how to obtain the parameter value.

_Type_: **[ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#parameter1type) __nullable__**  
Generic enum type for ActionParameterType properties  
_Allowed Values (Systems.Bpm.ActionParameterType Enum Members)_  

| Value | Description |
| ---- | --- |
| Constant | Constant value. Stored as 'CONST'. <br /> _Database Value:_ 'CONST' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Constant' |
| Attribute | Attribute value. Stored as 'ATTRIB'. <br /> _Database Value:_ 'ATTRIB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Attribute' |
| Reference | Reference value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Reference' |
| ChildList | ChildList value. Stored as 'CHILD'. <br /> _Database Value:_ 'CHILD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ChildList' |
| FormattedString | FormattedString value. Stored as 'FMTSTR'. <br /> _Database Value:_ 'FMTSTR' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'FormattedString' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter1Value

The actual value of the parameter.

_Type_: **string (256) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Parameter2Type

The type of the parameter specifies how to obtain the parameter value.

_Type_: **[ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#parameter2type) __nullable__**  
Generic enum type for ActionParameterType properties  
_Allowed Values (Systems.Bpm.ActionParameterType Enum Members)_  

| Value | Description |
| ---- | --- |
| Constant | Constant value. Stored as 'CONST'. <br /> _Database Value:_ 'CONST' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Constant' |
| Attribute | Attribute value. Stored as 'ATTRIB'. <br /> _Database Value:_ 'ATTRIB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Attribute' |
| Reference | Reference value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Reference' |
| ChildList | ChildList value. Stored as 'CHILD'. <br /> _Database Value:_ 'CHILD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ChildList' |
| FormattedString | FormattedString value. Stored as 'FMTSTR'. <br /> _Database Value:_ 'FMTSTR' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'FormattedString' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter2Value

The actual value of the parameter.

_Type_: **string (256) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Parameter3Type

The type of the parameter specifies how to obtain the parameter value.

_Type_: **[ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#parameter3type) __nullable__**  
Generic enum type for ActionParameterType properties  
_Allowed Values (Systems.Bpm.ActionParameterType Enum Members)_  

| Value | Description |
| ---- | --- |
| Constant | Constant value. Stored as 'CONST'. <br /> _Database Value:_ 'CONST' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Constant' |
| Attribute | Attribute value. Stored as 'ATTRIB'. <br /> _Database Value:_ 'ATTRIB' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Attribute' |
| Reference | Reference value. Stored as 'REF'. <br /> _Database Value:_ 'REF' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Reference' |
| ChildList | ChildList value. Stored as 'CHILD'. <br /> _Database Value:_ 'CHILD' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ChildList' |
| FormattedString | FormattedString value. Stored as 'FMTSTR'. <br /> _Database Value:_ 'FMTSTR' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'FormattedString' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter3Value

The actual value of the parameter.

_Type_: **string (256) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  


## Reference Details

### UserBusinessRule

The business rule, for which the action is defined. `Required` `Filter(multi eq)` `Owner`

_Type_: **[UserBusinessRules](Systems.Bpm.UserBusinessRules.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.UserBusinessRuleActions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.UserBusinessRuleActions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_UserBusinessRuleActions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_UserBusinessRuleActions?$top=10>

