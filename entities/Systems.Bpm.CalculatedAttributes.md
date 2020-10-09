---
uid: Systems.Bpm.CalculatedAttributes
---
# Systems.Bpm.CalculatedAttributes Entity

User-defined read-only calculated attribute. Entity: Sys_Calculated_Attributes

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Caption](Systems.Bpm.CalculatedAttributes.md#caption) | [MultilanguageString](../data-types.md#multilanguagestring) | The multi-language caption, used to display the attribute. [Required] 
| [Id](Systems.Bpm.CalculatedAttributes.md#id) | guid |  
| [IsActive](Systems.Bpm.CalculatedAttributes.md#isactive) | boolean | True if the attribute is activated and added to the repository. [Required] [Default(false)] 
| [Name](Systems.Bpm.CalculatedAttributes.md#name) | string | The unique name of the attribute within the repository. [Required] [Filter(eq;like)] 
| [Notes](Systems.Bpm.CalculatedAttributes.md#notes) | string (nullable) | Notes for this CalculatedAttribute. 
| [RepositoryName](Systems.Bpm.CalculatedAttributes.md#repositoryname) | string | The repository, for which the attribute is defined. [Required] [Filter(multi eq)] [ORD] 
| [StartingExpressionNo](Systems.Bpm.CalculatedAttributes.md#startingexpressionno) | int32 | The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute. [Required] [Default(10)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Expressions | [CalculatedAttributeExpressions](Systems.Bpm.CalculatedAttributeExpressions.md) | List of [CalculatedAttribute<br />Expression](Systems.Bpm.CalculatedAttribute<br />Expressions.md) child objects, based on the [Systems.Bpm.CalculatedAttribute<br />Expression.CalculatedAttribute](Systems.Bpm.CalculatedAttribute<br />Expressions.md#calculatedattribute) back  


## Attribute Details

### Caption

The multi-language caption, used to display the attribute. [Required]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the attribute is activated and added to the repository. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The unique name of the attribute within the repository. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this CalculatedAttribute.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RepositoryName

The repository, for which the attribute is defined. [Required] [Filter(multi eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  

### StartingExpressionNo

The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute. [Required] [Default(10)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **10**  



## Business Rules

[!list erp.entity=Systems.Bpm.CalculatedAttributes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Bpm.CalculatedAttributes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_CalculatedAttributes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_CalculatedAttributes?$top=10>

