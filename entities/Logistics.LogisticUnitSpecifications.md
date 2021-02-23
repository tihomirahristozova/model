---
uid: Logistics.LogisticUnitSpecifications
---
# Logistics.LogisticUnitSpecifications Entity

Specification of a logistic unit. The database can contain any kind of specification, but most client applications and integrated methods process GS1 specifications (application codes). Entity: Log_Logistic_Unit_Specifications (Introduced in version 21.1.0.77)

Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

Aggregate Parent:  
[Logistics.LogisticUnits](Logistics.LogisticUnits.md)  
Aggregate Root:  
[Logistics.LogisticUnits](Logistics.LogisticUnits.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.LogisticUnitSpecifications.md#code) | string | The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces. [Required] [Filter(multi eq;like)] 
| [Id](Logistics.LogisticUnitSpecifications.md#id) | guid |  
| [Name](Logistics.LogisticUnitSpecifications.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) (nullable) | Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (null). [Filter(eq;like)] 
| [Notes](Logistics.LogisticUnitSpecifications.md#notes) | string (nullable) | Notes for this LogisticUnitSpecification. 
| [Value](Logistics.LogisticUnitSpecifications.md#value) | string (nullable) | Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces. [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LogisticUnit](Logistics.LogisticUnitSpecifications.md#logisticunit) | [LogisticUnits](Logistics.LogisticUnits.md) | The logistic unit, which is detailed by this specification. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Code

The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (null). [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this LogisticUnitSpecification.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Value

Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### LogisticUnit

The logistic unit, which is detailed by this specification. [Required] [Filter(multi eq)] [Owner]

_Type_: **[LogisticUnits](Logistics.LogisticUnits.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.LogisticUnitSpecifications erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.LogisticUnitSpecifications erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_LogisticUnitSpecifications?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_LogisticUnitSpecifications?$top=10>

