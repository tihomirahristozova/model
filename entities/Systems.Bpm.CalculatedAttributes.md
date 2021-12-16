---
uid: Systems.Bpm.CalculatedAttributes
---
# Systems.Bpm.CalculatedAttributes Entity

**Namespace:** [Systems.Bpm](Systems.Bpm.md)  

User-defined read-only calculated attribute. Entity: Sys_Calculated_Attributes

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Bpm.CalculatedAttributes](Systems.Bpm.CalculatedAttributes.md)  
  * [Systems.Bpm.CalculatedAttributeExpressions](Systems.Bpm.CalculatedAttributeExpressions.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Caption](Systems.Bpm.CalculatedAttributes.md#caption) | [MultilanguageString](../data-types.md#multilanguagestring) | The multi-language caption, used to display the attribute. `Required` 
| [Hint](Systems.Bpm.CalculatedAttributes.md#hint) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | The hint, which is displayed alongside the attribute. `Filter(multi eq;like)` `Introduced in version 21.1.3.53` 
| [Id](Systems.Bpm.CalculatedAttributes.md#id) | guid |  
| [IsActive](Systems.Bpm.CalculatedAttributes.md#isactive) | boolean | True if the attribute is activated and added to the repository. `Required` `Default(false)` 
| [Name](Systems.Bpm.CalculatedAttributes.md#name) | string (128) | The unique name of the attribute within the repository. `Required` `Filter(eq;like)` 
| [Notes](Systems.Bpm.CalculatedAttributes.md#notes) | string (max) __nullable__ | Notes for this CalculatedAttribute. 
| [RepositoryName](Systems.Bpm.CalculatedAttributes.md#repositoryname) | string (128) | The repository, for which the attribute is defined. `Required` `Filter(multi eq)` `ORD` 
| [RowVersion](Systems.Bpm.CalculatedAttributes.md#rowversion) | byte[] |  
| [StartingExpressionNo](Systems.Bpm.CalculatedAttributes.md#startingexpressionno) | int32 | The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute. `Required` `Default(10)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Expressions | [CalculatedAttributeExpressions](Systems.Bpm.CalculatedAttributeExpressions.md) | List of `CalculatedAttribute<br />Expression`(Systems.Bpm.CalculatedAttribute<br />Expressions.md) child objects, based on the `Systems.Bpm.CalculatedAttribute<br />Expression.CalculatedAttribute`(Systems.Bpm.CalculatedAttribute<br />Expressions.md#calculatedattribute) back reference 


## Attribute Details

### Caption

The multi-language caption, used to display the attribute. `Required`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Hint

The hint, which is displayed alongside the attribute. `Filter(multi eq;like)` `Introduced in version 21.1.3.53`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the attribute is activated and added to the repository. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The unique name of the attribute within the repository. `Required` `Filter(eq;like)`

_Type_: **string (128)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### Notes

Notes for this CalculatedAttribute.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RepositoryName

The repository, for which the attribute is defined. `Required` `Filter(multi eq)` `ORD`

_Type_: **string (128)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **128**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartingExpressionNo

The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute. `Required` `Default(10)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **10**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.CalculatedAttributes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.CalculatedAttributes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_CalculatedAttributes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_CalculatedAttributes?$top=10>

