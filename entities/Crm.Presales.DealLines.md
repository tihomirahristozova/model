---
uid: Crm.Presales.DealLines
---
# Crm.Presales.DealLines Entity

**Namespace:** [Crm.Presales](Crm.Presales.md)  

Detail records (lines) of the deals. Entity: Crm_Deal_Lines (Introduced in version 22.1.4.53)

## Default Visualization
Default Display Text Format:  
_{Deal.EntityName}_  
Default Search Members:  
_Deal.EntityName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Crm.Presales.Deals](Crm.Presales.Deals.md)  
Aggregate Root:  
[Crm.Presales.Deals](Crm.Presales.Deals.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Presales.DealLines.md#id) | guid |  
| [LineNo](Crm.Presales.DealLines.md#lineno) | int32 | Consecutive number of the line within the deal. `Required` `Filter(eq)` 
| [Notes](Crm.Presales.DealLines.md#notes) | string (max) __nullable__ | Notes. 
| [Quantity](Crm.Presales.DealLines.md#quantity) | [Quantity (12, 3)](../data-types.md#quantity) __nullable__ | When not null, specifies the quantity, which the client can potentially buy (with measurement unit specified in Quantity Unit). `Unit: QuantityUnit` 
| [RowVersion](Crm.Presales.DealLines.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Deal](Crm.Presales.DealLines.md#deal) | [Deals](Crm.Presales.Deals.md) | Deal. `Required` `Filter(multi eq)` `Owner` |
| [Product](Crm.Presales.DealLines.md#product) | [Products](General.Products.Products.md) | The product, to which the client has interest. `Required` `Filter(multi eq)` |
| [QuantityUnit](Crm.Presales.DealLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Consecutive number of the line within the deal. `Required` `Filter(eq)`

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Deal.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Deal.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Quantity

When not null, specifies the quantity, which the client can potentially buy (with measurement unit specified in Quantity Unit). `Unit: QuantityUnit`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Deal

Deal. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Deals](Crm.Presales.Deals.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### Product

The product, to which the client has interest. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.Product.MeasurementUnit`


## Business Rules

[!list limit=1000 erp.entity=Crm.Presales.DealLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Presales.DealLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Presales_DealLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Presales_DealLines?$top=10>

