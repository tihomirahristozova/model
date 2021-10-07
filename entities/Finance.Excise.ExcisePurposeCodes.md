---
uid: Finance.Excise.ExcisePurposeCodes
---
# Finance.Excise.ExcisePurposeCodes Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Purpose codes specify the different purposes recognized by the authorities for determining the excise rate. Entity: Exc_Excise_Purpose_Codes (Introduced in version 21.1.3.87)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExcisePurposeCodes](Finance.Excise.ExcisePurposeCodes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Excise.ExcisePurposeCodes.md#code) | string (32) | The unique code of the ExcisePurposeCode. `Required` `Filter(eq;like)` `ORD` 
| [Id](Finance.Excise.ExcisePurposeCodes.md#id) | guid |  
| [IsDefault](Finance.Excise.ExcisePurposeCodes.md#isdefault) | boolean | Excise Purpose Codes which is the default for documents. `Required` `Default(false)` `Filter(eq)` `Introduced in version 21.1.4.0` 
| [Name](Finance.Excise.ExcisePurposeCodes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this ExcisePurposeCode. `Required` `Filter(like)` 
| [Notes](Finance.Excise.ExcisePurposeCodes.md#notes) | string (max) __nullable__ | Notes for this ExcisePurposeCode. 


## Attribute Details

### Code

The unique code of the ExcisePurposeCode. `Required` `Filter(eq;like)` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

Excise Purpose Codes which is the default for documents. `Required` `Default(false)` `Filter(eq)` `Introduced in version 21.1.4.0`

_Type_: **boolean**  
_Indexed_: **True**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The name of this ExcisePurposeCode. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this ExcisePurposeCode.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExcisePurposeCodes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExcisePurposeCodes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExcisePurposeCodes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExcisePurposeCodes?$top=10>

