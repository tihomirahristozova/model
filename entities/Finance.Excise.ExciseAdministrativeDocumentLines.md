---
uid: Finance.Excise.ExciseAdministrativeDocumentLines
---
# Finance.Excise.ExciseAdministrativeDocumentLines Entity

**Namespace:** [Finance.Excise](Finance.Excise.md)  

The details of the movement of each excise product for each excise document. Entity: Exc_Excise_Administrative_Document_Lines (Introduced in version 21.1.3.54)

## Default Visualization
Default Display Text Format:  
_{ExciseAdministrativeDocument.DocumentType.Code}:{ExciseAdministrativeDocument.DocumentNo}:{LineNo} - {ExciseAdministrativeDocument.DocumentType.TypeName:T}_  
Default Search Member:  
_ExciseAdministrativeDocument.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Finance.Excise.ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md)  
Aggregate Root:  
[Finance.Excise.ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Finance.Excise.ExciseAdministrativeDocumentLines.md#id) | guid |  
| [LineNo](Finance.Excise.ExciseAdministrativeDocumentLines.md#lineno) | int32 | Consecutive line number within the document. `Required` 
| [Notes](Finance.Excise.ExciseAdministrativeDocumentLines.md#notes) | string (max) __nullable__ | Notes for this ExciseAdministrative<br />DocumentLine. 
| [Quantity](Finance.Excise.ExciseAdministrativeDocumentLines.md#quantity) | [Quantity (12, 3)](../data-types.md#quantity) | The quantity being sold, in the measurement unit, specified in Quantity Unit. `Unit: QuantityUnit` `Required` `Default(1)` 
| [QuantityBase](Finance.Excise.ExciseAdministrativeDocumentLines.md#quantitybase) | [Quantity (12, 3)](../data-types.md#quantity) | The quantity in base measurement category for the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Finance.Excise.ExciseAdministrativeDocumentLines.md#document) | [ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md) | The `ExciseAdministrative<br />Document`(Finance.Excise.ExciseAdministrative<br />DocumentLines.md#exciseadministrativedocument) to which this ExciseAdministrative<br />DocumentLine belongs. `Required` `Filter(multi eq)` |
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

_Back-End Default Expression:_  
`( obj.ExciseAdministrativeDocument.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ExciseAdministrativeDocument.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this ExciseAdministrativeDocumentLine.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Quantity

The quantity being sold, in the measurement unit, specified in Quantity Unit. `Unit: QuantityUnit` `Required` `Default(1)`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

The quantity in base measurement category for the product. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Document

The `ExciseAdministrativeDocument`(Finance.Excise.ExciseAdministrativeDocumentLines.md#exciseadministrativedocument) to which this ExciseAdministrativeDocumentLine belongs. `Required` `Filter(multi eq)`

_Type_: **[ExciseAdministrativeDocuments](Finance.Excise.ExciseAdministrativeDocuments.md)**  
_Supported Filters_: **Equals, EqualsIn**  

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

