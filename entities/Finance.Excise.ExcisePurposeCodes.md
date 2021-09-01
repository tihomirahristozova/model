---
uid: Finance.Excise.ExcisePurposeCodes
---
# Finance.Excise.ExcisePurposeCodes Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Purpose codes specify the different purposes recognized by the authorities for determining the excise rate. Entity: Exc_Excise_Purpose_Codes

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExcisePurposeCodes](Finance.Excise.ExcisePurposeCodes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Excise.ExcisePurposeCodes.md#code) | string (32) | The unique code of the ExcisePurposeCode. `Required` `ORD` 
| [Id](Finance.Excise.ExcisePurposeCodes.md#id) | guid |  
| [Name](Finance.Excise.ExcisePurposeCodes.md#name) | string (254) | The name of this ExcisePurposeCode. `Required` 
| [Notes](Finance.Excise.ExcisePurposeCodes.md#notes) | string (max) __nullable__ | Notes for this ExcisePurposeCode. 


## Attribute Details

### Code

The unique code of the ExcisePurposeCode. `Required` `ORD`

_Type_: **string (32)**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  
_Maximum Length_: **32**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this ExcisePurposeCode. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

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
