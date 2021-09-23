---
uid: General.DocumentTypeSecurityConditions
---
# General.DocumentTypeSecurityConditions Entity

**Namespace:** [General](General.md)  

Provides rules to conditionally secure new documents. Entity: Gen_Document_Type_Security_Conditions

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.DocumentTypeSecurityConditions](General.DocumentTypeSecurityConditions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConditionFilterXml](General.DocumentTypeSecurityConditions.md#conditionfilterxml) | dataaccessfilter | Specifies the documents, for which the current rule is applicable. The XML filter is compared against new documents and the rule is applicable when they match. `Required` 
| [Description](General.DocumentTypeSecurityConditions.md#description) | string (254) | The description of this DocumentTypeSecurity<br />Condition. `Required` `Filter(eq;like)` 
| [Id](General.DocumentTypeSecurityConditions.md#id) | guid |  
| [Priority](General.DocumentTypeSecurityConditions.md#priority) | [Priority](General.DocumentTypeSecurityConditions.md#priority) | Priority of the rule against other rules, which are also applicable. Only the highest priority rule is selected. `Required` `Default(3)` `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAccessKey](General.DocumentTypeSecurityConditions.md#documentaccesskey) | [AccessKeys](Systems.Security.AccessKeys.md) | The access key, which will be used to secure new documents, when this rule is selected. `Required` `Filter(multi eq)` |
| [DocumentType](General.DocumentTypeSecurityConditions.md#documenttype) | [DocumentTypes](General.DocumentTypes.md) | The document type, whose documents will be secured by the current rule. `Required` `Filter(multi eq)` |


## Attribute Details

### ConditionFilterXml

Specifies the documents, for which the current rule is applicable. The XML filter is compared against new documents and the rule is applicable when they match. `Required`

_Type_: **dataaccessfilter**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

The description of this DocumentTypeSecurityCondition. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Priority

Priority of the rule against other rules, which are also applicable. Only the highest priority rule is selected. `Required` `Default(3)` `Filter(ge;le)`

_Type_: **[Priority](General.DocumentTypeSecurityConditions.md#priority)**  
Generic enum type for Priority properties  
_Allowed Values (General.Priority Enum Members)_  

| Value | Description |
| ---- | --- |
| Lowest | Lowest value. Stored as 1. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Lowest' |
| Low | Low value. Stored as 2. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Low' |
| Medium | Medium value. Stored as 3. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Medium' |
| High | High value. Stored as 4. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'High' |
| Highest | Highest value. Stored as 5. <br /> _Database Value:_ 5 <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Highest' |

_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **3**  


## Reference Details

### DocumentAccessKey

The access key, which will be used to secure new documents, when this rule is selected. `Required` `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentType

The document type, whose documents will be secured by the current rule. `Required` `Filter(multi eq)`

_Type_: **[DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeSecurityConditions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentTypeSecurityConditions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeSecurityConditions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeSecurityConditions?$top=10>

