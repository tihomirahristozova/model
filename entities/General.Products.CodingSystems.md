---
uid: General.Products.CodingSystems
---
# General.Products.CodingSystems Entity

**Namespace:** [General.Products](General.Products.md)  

Coding systems categorize additional product codes. Entity: Gen_Coding_Systems

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Products.CodingSystems](General.Products.CodingSystems.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](General.Products.CodingSystems.md#description) | string (max) __nullable__ | The description of this CodingSystem. 
| [Id](General.Products.CodingSystems.md#id) | guid |  
| [IsUnique](General.Products.CodingSystems.md#isunique) | boolean | True when the coding system can contain only unique product codes. false - duplicate product codes are allowed. `Required` `Default(true)` `Filter(eq)` 
| [Name](General.Products.CodingSystems.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this CodingSystem. `Required` `Filter(eq;like)` 
| [ObjectVersion](General.Products.CodingSystems.md#objectversion) | int32 |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultMeasurementUnit](General.Products.CodingSystems.md#defaultmeasurementunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | When not null, specifies a measurement unit to be used as default, instead of the products default unit. `Filter(multi eq)` |


## Attribute Details

### Description

The description of this CodingSystem.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsUnique

True when the coding system can contain only unique product codes. false - duplicate product codes are allowed. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of this CodingSystem. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  


## Reference Details

### DefaultMeasurementUnit

When not null, specifies a measurement unit to be used as default, instead of the products default unit. `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.CodingSystems erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.CodingSystems erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_CodingSystems?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_CodingSystems?$top=10>

