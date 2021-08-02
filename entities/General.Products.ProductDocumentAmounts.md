---
uid: General.Products.ProductDocumentAmounts
---
# General.Products.ProductDocumentAmounts Entity

**Namespace:** [General.Products](General.Products.md)  

Contains custom percent ratios for additional amount distribution over products. Entity: Gen_Product_Document_Amounts

## Default Visualization
Default Display Text Format:  
_{Product.PartNumber}: {Product.Name:T}_  
Default Search Member:  
_Product.PartNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.Products](General.Products.Products.md)  
Aggregate Root:  
[General.Products.Products](General.Products.Products.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductDocumentAmounts.md#id) | guid |  
| [LinePercent](General.Products.ProductDocumentAmounts.md#linepercent) | decimal (14, 3) | The custom percent for the current product and amount type. `Required` `Default(0)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DocumentAmountType](General.Products.ProductDocumentAmounts.md#documentamounttype) | [DocumentAmountTypes](General.DocumentAmountTypes.md) | The amount type for which the custom percent is defined. `Required` `Filter(multi eq)` |
| [Product](General.Products.ProductDocumentAmounts.md#product) | [Products](General.Products.Products.md) | The `Product`(General.Products.ProductDocumentAmounts.md#product) to which this ProductDocumentAmount belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LinePercent

The custom percent for the current product and amount type. `Required` `Default(0)`

_Type_: **decimal (14, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### DocumentAmountType

The amount type for which the custom percent is defined. `Required` `Filter(multi eq)`

_Type_: **[DocumentAmountTypes](General.DocumentAmountTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The `Product`(General.Products.ProductDocumentAmounts.md#product) to which this ProductDocumentAmount belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.ProductDocumentAmounts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.ProductDocumentAmounts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductDocumentAmounts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductDocumentAmounts?$top=10>

