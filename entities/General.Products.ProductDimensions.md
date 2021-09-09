---
uid: General.Products.ProductDimensions
---
# General.Products.ProductDimensions Entity

**Namespace:** [General.Products](General.Products.md)  

Contains convertion ratios between the supported measument categories for each product. Does not contain a record for the default category of the products, for which the convertion ratio is defined as equal to 1. Entity: Gen_Product_Dimensions

## Default Visualization
Default Display Text Format:  
_{Product.Name:T} : {Product.PartNumber}_  
Default Search Member:  
_Product.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Products.Products](General.Products.Products.md)  
Aggregate Root:  
[General.Products.Products](General.Products.Products.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConvertToBaseDivisor](General.Products.ProductDimensions.md#converttobasedivisor) | decimal (9, 3) | This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. `Required` 
| [ConvertToBaseMultiplier](General.Products.ProductDimensions.md#converttobasemultiplier) | decimal (9, 3) | This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. `Required` 
| [DestQuantity](General.Products.ProductDimensions.md#destquantity) | [Quantity (9, 3)](../data-types.md#quantity) | Quantity in some of the base units, that equals Source_Quantity. `Unit: DestQuantityUnit` `Required` `Default(1)` 
| [Id](General.Products.ProductDimensions.md#id) | guid |  
| [SourceQuantity](General.Products.ProductDimensions.md#sourcequantity) | [Quantity (9, 3)](../data-types.md#quantity) | The quantity in the non-base unit. `Unit: SourceQuantityUnit` `Required` `Default(1)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DestQuantityUnit](General.Products.ProductDimensions.md#destquantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Dest_Quantity. Should be one of the units of the base measurement category of the product. `Required` `Filter(multi eq)` |
| [MeasurementCategory](General.Products.ProductDimensions.md#measurementcategory) | [MeasurementCategories](General.MeasurementCategories.md) | The measurement category of Source Quantity Unit. For each product, only one conversion ratio can be specified for a measurement category. `Required` `Filter(multi eq)` `ReadOnly` |
| [Product](General.Products.ProductDimensions.md#product) | [Products](General.Products.Products.md) | The product for which we specify conversion ratios. `Required` `Filter(multi eq)` `Owner` |
| [SourceQuantityUnit](General.Products.ProductDimensions.md#sourcequantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The non-base measurement unit for which we specify convertion ratio. `Required` `Filter(multi eq)` |


## Attribute Details

### ConvertToBaseDivisor

This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. `Required`

_Type_: **decimal (9, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( ( obj.DestQuantity.Value * obj.DestQuantityUnit.Multiplier) * obj.SourceQuantityUnit.Divisor)`

_Front-End Recalc Expressions:_  
`( ( obj.DestQuantity.Value * obj.DestQuantityUnit.Multiplier) * obj.SourceQuantityUnit.Divisor)`
### ConvertToBaseMultiplier

This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. `Required`

_Type_: **decimal (9, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( ( obj.SourceQuantity.Value * obj.SourceQuantityUnit.Multiplier) * obj.DestQuantityUnit.Divisor)`

_Front-End Recalc Expressions:_  
`( ( obj.SourceQuantity.Value * obj.SourceQuantityUnit.Multiplier) * obj.DestQuantityUnit.Divisor)`
### DestQuantity

Quantity in some of the base units, that equals Source_Quantity. `Unit: DestQuantityUnit` `Required` `Default(1)`

_Type_: **[Quantity (9, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### SourceQuantity

The quantity in the non-base unit. `Unit: SourceQuantityUnit` `Required` `Default(1)`

_Type_: **[Quantity (9, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### DestQuantityUnit

The measurement unit of Dest_Quantity. Should be one of the units of the base measurement category of the product. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MeasurementCategory

The measurement category of Source Quantity Unit. For each product, only one conversion ratio can be specified for a measurement category. `Required` `Filter(multi eq)` `ReadOnly`

_Type_: **[MeasurementCategories](General.MeasurementCategories.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Back-End Default Expression:_  
`obj.SourceQuantityUnit.MeasurementCategory`

_Front-End Recalc Expressions:_  
`obj.SourceQuantityUnit.MeasurementCategory`
### Product

The product for which we specify conversion ratios. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### SourceQuantityUnit

The non-base measurement unit for which we specify convertion ratio. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=General.Products.ProductDimensions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Products.ProductDimensions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductDimensions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductDimensions?$top=10>

