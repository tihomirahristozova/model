---
uid: General.Products.CodingSystems
---
# General.Products.CodingSystems Entity

Coding systems categorize additional product codes. Entity: Gen_Coding_Systems

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](General.Products.CodingSystems.md#description) | string (nullable) | The description of this CodingSystem. 
| [Id](General.Products.CodingSystems.md#id) | guid |  
| [IsUnique](General.Products.CodingSystems.md#isunique) | boolean | True when the coding system can contain only unique product codes. false - duplicate product codes are allowed. [Required] [Default(true)] [Filter(eq)] 
| [Name](General.Products.CodingSystems.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this CodingSystem. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultMeasurementUnit](General.Products.CodingSystems.md#defaultmeasurementunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | When not null, specifies a measurement unit to be used as default, instead of the products default unit. [Filter(multi eq)] |


## Attribute Details

### Description

The description of this CodingSystem.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsUnique

True when the coding system can contain only unique product codes. false - duplicate product codes are allowed. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

The name of this CodingSystem. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### DefaultMeasurementUnit

When not null, specifies a measurement unit to be used as default, instead of the products default unit. [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Products.CodingSystems erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.CodingSystems erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_CodingSystems?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_CodingSystems?$top=10>

