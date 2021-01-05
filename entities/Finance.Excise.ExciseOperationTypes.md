---
uid: Finance.Excise.ExciseOperationTypes
---
# Finance.Excise.ExciseOperationTypes Entity

Types of excise operations. Used by general documents to specify the operation type according to the excise classifications. Entity: Exc_Excise_Operation_Types (Introduced in version 21.1.1.59)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Finance.Excise.ExciseOperationTypes.md#code) | string | The unique code of the ExciseOperationType. [Required] [Filter(multi eq;like)] 
| [Id](Finance.Excise.ExciseOperationTypes.md#id) | guid |  
| [Name](Finance.Excise.ExciseOperationTypes.md#name) | string | The name of this ExciseOperationType. [Required] [Filter(multi eq;like)] 
| [Notes](Finance.Excise.ExciseOperationTypes.md#notes) | string (nullable) | Notes for this ExciseOperationType. 


## Attribute Details

### Code

The unique code of the ExciseOperationType. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this ExciseOperationType. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

Notes for this ExciseOperationType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Finance.Excise.ExciseOperationTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Excise.ExciseOperationTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseOperationTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseOperationTypes?$top=10>

