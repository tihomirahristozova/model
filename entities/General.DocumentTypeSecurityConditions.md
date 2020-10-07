# General.DocumentTypeSecurityConditions

Provides rules to conditionally secure new documents. Entity: Gen_Document_Type_Security_Conditions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentTypeSecurityConditions.md#Id) | guid |  
| [ConditionFilterXml](General.DocumentTypeSecurityConditions.md#ConditionFilterXml) | dataaccessfilter | Specifies the documents, for which the current rule is applicable. The XML filter is compared against new documents and the rule is applicable when they match. [Required] 
| [Description](General.DocumentTypeSecurityConditions.md#Description) | string | The description of this DocumentTypeSecurityCondition. [Required] [Filter(eq;like)] 
| [Priority](General.DocumentTypeSecurityConditions.md#Priority) | [General.Priority](General.DocumentTypeSecurityConditions.md#Priority) | Priority of the rule against other rules, which are also applicable. Only the highest priority rule is selected. [Required] [Default(3)] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAccessKey](General.DocumentTypeSecurityConditions.md#DocumentAccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) | The access key, which will be used to secure new documents, when this rule is selected. [Required] [Filter(multi eq)] |
| [DocumentType](General.DocumentTypeSecurityConditions.md#DocumentType) | [General.DocumentTypes](General.DocumentTypes.md) | The document type, whose documents will be secured by the current rule. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConditionFilterXml

> Specifies the documents, for which the current rule is applicable. The XML filter is compared against new documents and the rule is applicable when they match. [Required]

_Type_: **dataaccessfilter**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

> The description of this DocumentTypeSecurityCondition. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Priority

> Priority of the rule against other rules, which are also applicable. Only the highest priority rule is selected. [Required] [Default(3)] [Filter(ge;le)]

_Type_: **[General.Priority](General.DocumentTypeSecurityConditions.md#Priority)**  
Generic enum type for Priority properties  
_Allowed Values (Enum Members)_  

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

> The access key, which will be used to secure new documents, when this rule is selected. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### DocumentType

> The document type, whose documents will be secured by the current rule. [Required] [Filter(multi eq)]

_Type_: **[General.DocumentTypes](General.DocumentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.DocumentTypeSecurityConditions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentTypeSecurityConditions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.DocumentTypeSecurityConditions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentTypeSecurityConditions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentTypeSecurityConditions?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Document_Type_Security_Conditions?$top=10>

