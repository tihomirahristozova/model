---
uid: General.Products.ProductDimensions
---
# General.Products.ProductDimensions

Contains convertion ratios between the supported measument categories for each product. Does not contain a record for the default category of the products, for which the convertion ratio is defined as equal to 1. Entity: Gen_Product_Dimensions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductDimensions.md#Id) | guid |  
| [ConvertToBaseDivisor](General.Products.ProductDimensions.md#ConvertToBaseDivisor) | decimal | This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. [Required] 
| [ConvertToBaseMultiplier](General.Products.ProductDimensions.md#ConvertToBaseMultiplier) | decimal | This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. [Required] 
| [DestQuantity](General.Products.ProductDimensions.md#DestQuantity) | [Quantity](../data-types.md#Quantity) | Quantity in some of the base units, that equals Source_Quantity. [Unit: DestQuantityUnit] [Required] [Default(1)] 
| [SourceQuantity](General.Products.ProductDimensions.md#SourceQuantity) | [Quantity](../data-types.md#Quantity) | The quantity in the non-base unit. [Unit: SourceQuantityUnit] [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DestQuantityUnit](General.Products.ProductDimensions.md#DestQuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Dest_Quantity. Should be one of the units of the base measurement category of the product. [Required] [Filter(multi eq)] |
| [MeasurementCategory](General.Products.ProductDimensions.md#MeasurementCategory) | [General.MeasurementCategories](General.MeasurementCategories.md) | The measurement category of Source Quantity Unit. For each product, only one conversion ratio can be specified for a measurement category. [Required] [Filter(multi eq)] [ReadOnly] |
| [Product](General.Products.ProductDimensions.md#Product) | [General.Products.Products](General.Products.Products.md) | The product for which we specify conversion ratios. [Required] [Filter(multi eq)] [Owner] |
| [SourceQuantityUnit](General.Products.ProductDimensions.md#SourceQuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The non-base measurement unit for which we specify convertion ratio. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConvertToBaseDivisor

> This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`((obj.DestQuantity.Value * obj.DestQuantityUnit.Multiplier) * obj.SourceQuantityUnit.Divisor)`

_Front-End Recalc Expressions:_  
`((obj.DestQuantity.Value * obj.DestQuantityUnit.Multiplier) * obj.SourceQuantityUnit.Divisor)`
### ConvertToBaseMultiplier

> This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system. [Required]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`((obj.SourceQuantity.Value * obj.SourceQuantityUnit.Multiplier) * obj.DestQuantityUnit.Divisor)`

_Front-End Recalc Expressions:_  
`((obj.SourceQuantity.Value * obj.SourceQuantityUnit.Multiplier) * obj.DestQuantityUnit.Divisor)`
### DestQuantity

> Quantity in some of the base units, that equals Source_Quantity. [Unit: DestQuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### SourceQuantity

> The quantity in the non-base unit. [Unit: SourceQuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  


## Reference Details

### DestQuantityUnit

> The measurement unit of Dest_Quantity. Should be one of the units of the base measurement category of the product. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MeasurementCategory

> The measurement category of Source Quantity Unit. For each product, only one conversion ratio can be specified for a measurement category. [Required] [Filter(multi eq)] [ReadOnly]

_Type_: **[General.MeasurementCategories](General.MeasurementCategories.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.SourceQuantityUnit.MeasurementCategory`

_Front-End Recalc Expressions:_  
`obj.SourceQuantityUnit.MeasurementCategory`
### Product

> The product for which we specify conversion ratios. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SourceQuantityUnit

> The non-base measurement unit for which we specify convertion ratio. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=General.Products.ProductDimensions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductDimensions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.ProductDimensions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductDimensions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductDimensions?$top=10>

