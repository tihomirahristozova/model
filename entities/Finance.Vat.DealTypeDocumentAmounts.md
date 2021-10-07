---
uid: Finance.Vat.DealTypeDocumentAmounts
---
# Finance.Vat.DealTypeDocumentAmounts Entity

**Namespace:** [Finance.Vat](Finance.Vat.md)  

Contains custom percent ratios for additional amount distribution over products for VAT purposes. Entity: VAT_Deal_Type_Document_Amounts (Introduced in version 22.1.4.19)

## Default Visualization
Default Display Text Format:  
_{DealType.Name}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md)  
Aggregate Root:  
[Finance.Vat.DealTypes](Finance.Vat.DealTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Vat.DealTypeDocumentAmounts.md#id) | guid |  
| [LinePercent](Finance.Vat.DealTypeDocumentAmounts.md#linepercent) | decimal (14, 3) | Percent by which additional amount is calculated. `Required` `Default(0)` 
| [Notes](Finance.Vat.DealTypeDocumentAmounts.md#notes) | string (max) __nullable__ | Notes for this DealTypeDocumentAmount. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DealType](Finance.Vat.DealTypeDocumentAmounts.md#dealtype) | [DealTypes](Finance.Vat.DealTypes.md) | Deal type for which is calculated additional amount. `Required` `Filter(multi eq)` `ReadOnly` `Owner` |
| [DocumentAmountType](Finance.Vat.DealTypeDocumentAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | Type of additional amount which is calculated for the documents. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LinePercent

Percent by which additional amount is calculated. `Required` `Default(0)`

_Type_: **decimal (14, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Notes

Notes for this DealTypeDocumentAmount.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### DealType

Deal type for which is calculated additional amount. `Required` `Filter(multi eq)` `ReadOnly` `Owner`

_Type_: **[DealTypes](Finance.Vat.DealTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### DocumentAmountType

Type of additional amount which is calculated for the documents. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Finance.Vat.DealTypeDocumentAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Finance.Vat.DealTypeDocumentAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Vat_DealTypeDocumentAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Vat_DealTypeDocumentAmounts?$top=10>

