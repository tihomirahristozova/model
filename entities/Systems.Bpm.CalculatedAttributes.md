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
| [ObjectVersion](Systems.Bpm.CalculatedAttributes.md#objectversion) | int32 |  
| [RepositoryName](Systems.Bpm.CalculatedAttributes.md#repositoryname) | string (128) | The repository, for which the attribute is defined. `Required` `Filter(multi eq)` `ORD` 
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

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### RepositoryName

The repository, for which the attribute is defined. `Required` `Filter(multi eq)` `ORD`

_Type_: **string (128)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **128**  

### StartingExpressionNo

The expression, from which the calculation starts. The result of the expression gives the value of the calculated attribute. `Required` `Default(10)`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **10**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources does not support ordering.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.CalculatedAttributes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Bpm.CalculatedAttributes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Bpm_CalculatedAttributes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Bpm_CalculatedAttributes?$top=10>

