---
uid: General.DocumentLineAmounts
---
# General.DocumentLineAmounts Entity

**Namespace:** [General](General.md)  

Specifies user-defined distribution pattern of additonal amount for specific document. Entity: Gen_Document_Line_Amounts

## Default Visualization
Default Display Text Format:  
_{Document.DocumentType.Code}:{Document.DocumentNo} - {Document.DocumentType.TypeName:T}_  
Default Search Member:  
_Document.DocumentType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Documents](General.Documents.md)  
Aggregate Root:  
[General.Documents](General.Documents.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentLineId](General.DocumentLineAmounts.md#documentlineid) | guid | The line for which the distribution pattern is specified. `Required` `Filter(multi eq)` 
| [Id](General.DocumentLineAmounts.md#id) | guid |  
| [LinePercent](General.DocumentLineAmounts.md#linepercent) | decimal (14, 6) | The percent of the additional amount which should be distributed over the current line. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](General.DocumentLineAmounts.md#document) | [Documents](General.Documents.md) | The `Document`(General.DocumentLineAmounts.md#document) to which this DocumentLineAmount belongs. `Required` `Filter(multi eq)` `Owner` |
| [DocumentAmountType](General.DocumentLineAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The type of amount for which the distribution pattern is specified. `Required` `Filter(multi eq)` |
| [Product](General.DocumentLineAmounts.md#product) | [Products](General.Products.Products.md) | The product for which the distribution is specified. It is also the product, specified in the document line, but is duplicated here for integrity purposes. `Required` `Filter(multi eq)` |
| [ReferencedDocument](General.DocumentLineAmounts.md#referenceddocument) | [Documents](General.Documents.md) (nullable) | When not null, specifies that this distribution is specified for a referenced document (not the document for which the amount is calculated). `Filter(multi eq)` |


## Attribute Details

### DocumentLineId

The line for which the distribution pattern is specified. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LinePercent

The percent of the additional amount which should be distributed over the current line. `Required` `Default(0)`

_Type_: **decimal (14, 6)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### Document

The `Document`(General.DocumentLineAmounts.md#document) to which this DocumentLineAmount belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Documents](General.Documents.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### DocumentAmountType

The type of amount for which the distribution pattern is specified. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product for which the distribution is specified. It is also the product, specified in the document line, but is duplicated here for integrity purposes. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReferencedDocument

When not null, specifies that this distribution is specified for a referenced document (not the document for which the amount is calculated). `Filter(multi eq)`

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.DocumentLineAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.DocumentLineAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_DocumentLineAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_DocumentLineAmounts?$top=10>

