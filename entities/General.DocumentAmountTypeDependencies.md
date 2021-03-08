---
uid: General.DocumentAmountTypeDependencies
---
# General.DocumentAmountTypeDependencies Entity

**Namespace:** [General](General.md)  

Specifies the base amounts on which an amount depends. . Entity: Gen_Document_Amount_Type_Dependencies

## Default Visualization
Default Display Text Format:  
_{DocumentAmountType.AmountTypeCode}: {DocumentAmountType.AmountTypeName:T}_  
Default Search Member:  
_DocumentAmountType.AmountTypeCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.DocumentAmountTypes](General.DocumentAmountTypes.md)  
Aggregate Root:  
[General.DocumentAmountTypes](General.DocumentAmountTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.DocumentAmountTypeDependencies.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DependsOnDocument<br />AmountType](General.DocumentAmountTypeDependencies.md#dependsondocumentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The base amount type on which the current amount depends. `Required` `Filter(multi eq)` |
| [DocumentAmountType](General.DocumentAmountTypeDependencies.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount for which the base amount is specified. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DependsOnDocumentAmountType

The base amount type on which the current amount depends. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### DocumentAmountType

The amount for which the base amount is specified. `Required` `Filter(multi eq)` `Owner`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.DocumentAmountTypeDependencies erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.DocumentAmountTypeDependencies erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentAmountTypeDependencies?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentAmountTypeDependencies?$top=10>

