---
uid: Finance.Excise.ExciseAdministrativeDocumentLines
---
# Finance.Excise.ExciseAdministrativeDocumentLines Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

The details of the movement of each excise product for each excise document. Entity: Exc_Excise_Administrative_Document_Lines

## Default Visualization
Default Display Text Format:  
_{ExciseAdministrativeDocument.AdministrativeReferenceCode}_  
Default Search Member:  
_ExciseAdministrativeDocument.AdministrativeReferenceCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Excise.ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Excise.ExciseAdministrativeDocumentLines.md#id) | guid |  
| [LineNo](Finance.Excise.ExciseAdministrativeDocumentLines.md#lineno) | int32 | Consecutive line number within the document. `Required` 
| [Notes](Finance.Excise.ExciseAdministrativeDocumentLines.md#notes) | string (max) __nullable__ | Notes for this ExciseAdministrative<br />DocumentLine. 
| [Quantity](Finance.Excise.ExciseAdministrativeDocumentLines.md#quantity) | decimal (12, 3) | The quantity being sold, in the measurement unit, specified in Quantity Unit. `Required` `Default(1)` 
| [QuantityBase](Finance.Excise.ExciseAdministrativeDocumentLines.md#quantitybase) | decimal (12, 3) | The quantity in base measurement category for the product. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ExciseAdministrative<br />Document](Finance.Excise.ExciseAdministrativeDocumentLines.md#exciseadministrativedocument) | [ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md) | The `ExciseAdministrative<br />Document`(Finance.Excise.ExciseAdministrative<br />DocumentLines.md#exciseadministrativedocument) to which this ExciseAdministrative<br />DocumentLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [Product](Finance.Excise.ExciseAdministrativeDocumentLines.md#product) | [Products](General.Products.Products.md) | The product being sold. `Required` `Filter(multi eq)` |
| [QuantityUnit](Finance.Excise.ExciseAdministrativeDocumentLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive line number within the document. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this ExciseAdministrativeDocumentLine.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Quantity

The quantity being sold, in the measurement unit, specified in Quantity Unit. `Required` `Default(1)`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### QuantityBase

The quantity in base measurement category for the product. `Required`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ExciseAdministrativeDocument

The `ExciseAdministrativeDocument`(Finance.Excise.ExciseAdministrativeDocumentLines.md#exciseadministrativedocument) to which this ExciseAdministrativeDocumentLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Product

The product being sold. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Finance.Excise.ExciseAdministrativeDocumentLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Finance.Excise.ExciseAdministrativeDocumentLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Finance_Excise_ExciseAdministrativeDocumentLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Finance_Excise_ExciseAdministrativeDocumentLines?$top=10>

