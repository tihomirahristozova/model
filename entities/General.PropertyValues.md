---
uid: General.PropertyValues
---
# General.PropertyValues

The actual values of the user-defined properties for each actual entity. Entity: Gen_Property_Values

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.PropertyValues.md#Id) | guid |  
| [Description](General.PropertyValues.md#Description) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | The actual description value of the property for the specified entity (the entity with the specified Id). 
| [EntityItemId](General.PropertyValues.md#EntityItemId) | guid | The Id of the actual entity for which the value is specified. [Required] [Filter(multi eq)] 
| [Picture](General.PropertyValues.md#Picture) | byte[] (nullable) | The actual picture of the property for the specified entity (the entity with the specified Id). 
| [PropertyValueField](General.PropertyValues.md#PropertyValueField) | string (nullable) | The actual value of the property for the specified entity (the entity with the specified Id). 
| [ValueId](General.PropertyValues.md#ValueId) | guid (nullable) | The internal Id of the value of the property for the specified entity (the entity with the specified Id). For choosable properties, this contains the id of the original "allowed value" row, from which the value was derived. null for non-choosable (free-text) properties, but also for old property values (before this id was available) or other unknown values. [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Property](General.PropertyValues.md#Property) | [General.CustomProperties](General.CustomProperties.md) | The property, whose value is stored here. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Description

> The actual description value of the property for the specified entity (the entity with the specified Id).

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### EntityItemId

> The Id of the actual entity for which the value is specified. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Picture

> The actual picture of the property for the specified entity (the entity with the specified Id).

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyValueField

> The actual value of the property for the specified entity (the entity with the specified Id).

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValueId

> The internal Id of the value of the property for the specified entity (the entity with the specified Id). For choosable properties, this contains the id of the original "allowed value" row, from which the value was derived. null for non-choosable (free-text) properties, but also for old property values (before this id was available) or other unknown values. [Filter(multi eq)]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Property

> The property, whose value is stored here. [Required] [Filter(multi eq)]

_Type_: **[General.CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.PropertyValues erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.PropertyValues erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.PropertyValues erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertyValues?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertyValues?$top=10>

