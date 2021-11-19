---
uid: Systems.Bpm.UserBusinessRuleConditions
---
# Systems.Bpm.UserBusinessRuleConditions Entity

**Namespace:** [Systems.Bpm](Systems.Bpm.md)  

Represents one condition for the execution of a business rule. Entity: Sys_User_Business_Rule_Conditions

## Default Visualization
Default Display Text Format:  
_{AttributeName}_  
Default Search Members:  
_AttributeName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Bpm.UserBusinessRules](Systems.Bpm.UserBusinessRules.md)  
Aggregate Root:  
[Systems.Bpm.UserBusinessRules](Systems.Bpm.UserBusinessRules.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AttributeName](Systems.Bpm.UserBusinessRuleConditions.md#attributename) | string (64) | The attribute, which will be tested. `Required` 
| [ComparisonType](Systems.Bpm.UserBusinessRuleConditions.md#comparisontype) | [ComparisonType](Systems.Bpm.UserBusinessRuleConditions.md#comparisontype) | How to compare the attribute and the value of the condition - e.g. Attribute-Comparison-Value. `Required` `Default("Equals")` 
| [ConditionNo](Systems.Bpm.UserBusinessRuleConditions.md#conditionno) | int32 | Unique consecutive number of the condition within the business rule. `Required` 
| [Id](Systems.Bpm.UserBusinessRuleConditions.md#id) | guid |  
| [Notes](Systems.Bpm.UserBusinessRuleConditions.md#notes) | string (max) __nullable__ | Notes for this UserBusinessRuleCondition. `Introduced in version 20.1` 
| [Value](Systems.Bpm.UserBusinessRuleConditions.md#value) | string (254) __nullable__ | The value against which the data attribute will be tested. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [UserBusinessRule](Systems.Bpm.UserBusinessRuleConditions.md#userbusinessrule) | [UserBusinessRules](Systems.Bpm.UserBusinessRules.md) | The business rule, for which the condition is defined. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### AttributeName

The attribute, which will be tested. `Required`

_Type_: **string (64)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### ComparisonType

How to compare the attribute and the value of the condition - e.g. Attribute-Comparison-Value. `Required` `Default("Equals")`

_Type_: **[ComparisonType](Systems.Bpm.UserBusinessRuleConditions.md#comparisontype)**  
Allowed values for the `ComparisonType`(Systems.Bpm.UserBusinessRuleConditions.md#comparisontype) data attribute  
_Allowed Values (Systems.Bpm.UserBusinessRuleConditionsRepository.ComparisonType Enum Members)_  

| Value | Description |
| ---- | --- |
| Equals | Equals. Stored as 'Equals'. <br /> _Database Value:_ 'Equals' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Equals' |
| Greater_Than | Greater Than Or Equal. Stored as 'Greater_Than'. <br /> _Database Value:_ 'Greater_Than' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Greater_Than' |
| Less_Than | Less Than Or Equal. Stored as 'Less_Than'. <br /> _Database Value:_ 'Less_Than' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Less_Than' |
| Like | Compare by mask. Use * (asterisk) as wildcard char.. Stored as 'Like'. <br /> _Database Value:_ 'Like' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Like' |
| IsNull | Field is null.. Stored as 'IsNull'. <br /> _Database Value:_ 'IsNull' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'IsNull' |
| Not_Equals | Not Equals. Stored as 'Not_Equals'. <br /> _Database Value:_ 'Not_Equals' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Not_Equals' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Equals**  

### ConditionNo

Unique consecutive number of the condition within the business rule. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.UserBusinessRule.Conditions.Select( c => c.ConditionNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.UserBusinessRule.Conditions.Select( c => c.ConditionNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this UserBusinessRuleCondition. `Introduced in version 20.1`

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Value

The value against which the data attribute will be tested.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### UserBusinessRule

The business rule, for which the condition is defined. `Required` `Filter(multi eq)` `Owner`

_Type_: **[UserBusinessRules](Systems.Bpm.UserBusinessRules.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.UserBusinessRuleConditions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.UserBusinessRuleConditions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_UserBusinessRuleConditions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_UserBusinessRuleConditions?$top=10>

