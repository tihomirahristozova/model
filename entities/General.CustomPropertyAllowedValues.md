---
uid: General.CustomPropertyAllowedValues
---
# General.CustomPropertyAllowedValues Entity

**Namespace:** [General](General.md)  

User-defined properties allowed values. Can be specified only for properties with unbound allowed values (e.g. for which Allowed Values Entity is not set). Entity: Gen_Property_Allowed_Values

## Default Visualization
Default Display Text Format:  
_{Property.Code}: {Property.AllowedValuesEntityName:T}_  
Default Search Member:  
_Property.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.CustomProperties](General.CustomProperties.md)  
Aggregate Root:  
[General.CustomProperties](General.CustomProperties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Active](General.CustomPropertyAllowedValues.md#active) | boolean | Specifies whether the allowed value is active and can be used when selecting property values. `Required` `Default(true)` `Filter(eq)` 
| [Description](General.CustomPropertyAllowedValues.md#description) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table. `Filter(eq;like)` 
| [Id](General.CustomPropertyAllowedValues.md#id) | guid |  
| [LongDescription](General.CustomPropertyAllowedValues.md#longdescription) | string (max) __nullable__ | When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value. 
| [ParentAllowedValueId](General.CustomPropertyAllowedValues.md#parentallowedvalueid) | guid __nullable__ | The value of the parent property, for which this allowed value is valid. `Filter(multi eq)` 
| [Picture](General.CustomPropertyAllowedValues.md#picture) | byte[] __nullable__ | When not null, specifies a picture representation of the allowed value. 
| [PropertyAllowedValueField](General.CustomPropertyAllowedValues.md#propertyallowedvaluefield) | string (254) | The actual allowed value. `Required` `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](General.CustomPropertyAllowedValues.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this CustomPropertyAllowedValue applies, or null if it is for all enterprise companies. `Filter(multi eq)` |
| [Property](General.CustomPropertyAllowedValues.md#property) | [CustomProperties](General.CustomProperties.md) | The `CustomProperty`(General.CustomProperties.md) to which this CustomPropertyAllowedValue belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Active

Specifies whether the allowed value is active and can be used when selecting property values. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Description

The description of the property allowed value. Used to fill the Description column of the Property_Value in Gen_Property_Values_Table. `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LongDescription

When not null, specifies a long description of the allowed value. This long description is only used as helper information when selecting values, it is not copied in the property value.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ParentAllowedValueId

The value of the parent property, for which this allowed value is valid. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### Picture

When not null, specifies a picture representation of the allowed value.

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyAllowedValueField

The actual allowed value. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### EnterpriseCompany

The Enterprise Company to which this CustomPropertyAllowedValue applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

The `CustomProperty`(General.CustomProperties.md) to which this CustomPropertyAllowedValue belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  



## Business Rules

[!list erp.entity=General.CustomPropertyAllowedValues erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.CustomPropertyAllowedValues erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_CustomPropertyAllowedValues?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_CustomPropertyAllowedValues?$top=10>

