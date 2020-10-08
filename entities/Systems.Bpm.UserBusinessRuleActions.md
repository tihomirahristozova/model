---
uid: Systems.Bpm.UserBusinessRuleActions
---
# Systems.Bpm.UserBusinessRuleActions

Represents an action within a business rule. Entity: Sys_User_Business_Rule_Actions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Bpm.UserBusinessRuleActions.md#Id) | guid |  
| [ActionNo](Systems.Bpm.UserBusinessRuleActions.md#ActionNo) | int32 | Consecutive number of the action, unique within the business rule. [Required] 
| [ActionType](Systems.Bpm.UserBusinessRuleActions.md#ActionType) | [Systems.Bpm.UserBusinessRuleActionsRepository.ActionType](Systems.Bpm.UserBusinessRuleActions.md#ActionType) | Specifies the type of action to perform. [Required] 
| [Parameter1Type](Systems.Bpm.UserBusinessRuleActions.md#Parameter1Type) | [Systems.Bpm.ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#Parameter1Type) (nullable) | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter1Value](Systems.Bpm.UserBusinessRuleActions.md#Parameter1Value) | string (nullable) | The actual value of the parameter. 
| [Parameter2Type](Systems.Bpm.UserBusinessRuleActions.md#Parameter2Type) | [Systems.Bpm.ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#Parameter2Type) (nullable) | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter2Value](Systems.Bpm.UserBusinessRuleActions.md#Parameter2Value) | string (nullable) | The actual value of the parameter. 
| [Parameter3Type](Systems.Bpm.UserBusinessRuleActions.md#Parameter3Type) | [Systems.Bpm.ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#Parameter3Type) (nullable) | The type of the parameter specifies how to obtain the parameter value. 
| [Parameter3Value](Systems.Bpm.UserBusinessRuleActions.md#Parameter3Value) | string (nullable) | The actual value of the parameter. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [UserBusinessRule](Systems.Bpm.UserBusinessRuleActions.md#UserBusinessRule) | [Systems.Bpm.UserBusinessRules](Systems.Bpm.UserBusinessRules.md) | The business rule, for which the action is defined. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ActionNo

> Consecutive number of the action, unique within the business rule. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.UserBusinessRule.Actions.Select(c => c.ActionNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.UserBusinessRule.Actions.Select(c => c.ActionNo).DefaultIfEmpty(0).Max() + 10)`
### ActionType

> Specifies the type of action to perform. [Required]

_Type_: **[Systems.Bpm.UserBusinessRuleActionsRepository.ActionType](Systems.Bpm.UserBusinessRuleActions.md#ActionType)**  
Allowed values for the [ActionType](Systems.Bpm.UserBusinessRuleActions.md#ActionType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| SETVALUE | SETVALUE value. Stored as 'SETVALUE'. <br /> _Database Value:_ 'SETVALUE' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'SETVALUE' |
| FAIL | FAIL value. Stored as 'FAIL'. <br /> _Database Value:_ 'FAIL' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'FAIL' |
| SENDMAIL | SENDMAIL value. Stored as 'SENDMAIL'. <br /> _Database Value:_ 'SENDMAIL' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'SENDMAIL' |
| WARNING | WARNING value. Stored as 'WARNING'. <br /> _Database Value:_ 'WARNING' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'WARNING' |
| NOTIFYUSER | NOTIFYUSER value. Stored as 'NOTIFYUSER'. <br /> _Database Value:_ 'NOTIFYUSER' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'NOTIFYUSER' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter1Type

> The type of the parameter specifies how to obtain the parameter value.

_Type_: **[Systems.Bpm.ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#Parameter1Type) (nullable)**  
Generic enum type for ActionParameterType properties  
_Allowed Values (Enum Members)_  

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

> The actual value of the parameter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter2Type

> The type of the parameter specifies how to obtain the parameter value.

_Type_: **[Systems.Bpm.ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#Parameter2Type) (nullable)**  
Generic enum type for ActionParameterType properties  
_Allowed Values (Enum Members)_  

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

> The actual value of the parameter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Parameter3Type

> The type of the parameter specifies how to obtain the parameter value.

_Type_: **[Systems.Bpm.ActionParameterType](Systems.Bpm.UserBusinessRuleActions.md#Parameter3Type) (nullable)**  
Generic enum type for ActionParameterType properties  
_Allowed Values (Enum Members)_  

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

> The actual value of the parameter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### UserBusinessRule

> The business rule, for which the action is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Bpm.UserBusinessRules](Systems.Bpm.UserBusinessRules.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Bpm.UserBusinessRuleActions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.UserBusinessRuleActions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Bpm.UserBusinessRuleActions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_UserBusinessRuleActions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_UserBusinessRuleActions?$top=10>

