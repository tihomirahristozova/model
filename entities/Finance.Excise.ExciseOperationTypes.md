---
uid: Finance.Excise.ExciseOperationTypes
---
# Finance.Excise.ExciseOperationTypes Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

Types of excise operations. Used by general documents to specify the operation type according to the excise classifications. Entity: Exc_Excise_Operation_Types (Introduced in version 21.1.1.59)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Finance.Excise.ExciseOperationTypes](Finance.Excise.ExciseOperationTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Excise.ExciseOperationTypes.md#code) | string (16) | The unique code of the ExciseOperationType. `Required` `Filter(multi eq;like)` `ORD` 
| [Id](Finance.Excise.ExciseOperationTypes.md#id) | guid |  
| [Name](Finance.Excise.ExciseOperationTypes.md#name) | string (254) | The name of this ExciseOperationType. `Required` `Filter(multi eq;like)` 
| [Notes](Finance.Excise.ExciseOperationTypes.md#notes) | string (max) __nullable__ | Notes for this ExciseOperationType. 


## Attribute Details

### Code

The unique code of the ExciseOperationType. `Required` `Filter(multi eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this ExciseOperationType. `Required` `Filter(multi eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this ExciseOperationType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseOperationTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Excise.ExciseOperationTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseOperationTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseOperationTypes?$top=10>

