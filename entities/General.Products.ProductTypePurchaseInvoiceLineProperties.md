---
uid: General.Products.ProductTypePurchaseInvoiceLineProperties
---
# General.Products.ProductTypePurchaseInvoiceLineProperties Entity

When specified for a product type, contains the suggested user-defined properties, which can be specified when creating new purchase invoice lines with products of this type. Entity: Gen_Product_Type_Purchase_Invoice_Line_Properties

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductTypePurchaseInvoiceLineProperties.md#id) | guid |  
| [PropertyNo](General.Products.ProductTypePurchaseInvoiceLineProperties.md#propertyno) | int32 | The consecutive number (position) of the property within the current product type. [Required] 
| [Required](General.Products.ProductTypePurchaseInvoiceLineProperties.md#required) | boolean | True when the property is required, when creating new purchase invoice lines. False when this only suggests the usage of the property. [Required] [Default(false)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ProductType](General.Products.ProductTypePurchaseInvoiceLineProperties.md#producttype) | [ProductTypes](General.Products.ProductTypes.md) | The [ProductType](General.Products.ProductTypePurchase<br />InvoiceLineProperties.md#producttype) to which this ProductTypePurchase<br />InvoiceLineProperty belongs. [Required] [Filter(multi eq)]  |
| [Property](General.Products.ProductTypePurchaseInvoiceLineProperties.md#property) | [CustomProperties](General.CustomProperties.md) | The user-defined property. It should be with Entity Type = 'Purchase Invoice Line'. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### PropertyNo

The consecutive number (position) of the property within the current product type. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.ProductType.PurchaseInvoiceLineProperties.Select( c => c.PropertyNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.ProductType.PurchaseInvoiceLineProperties.Select( c => c.PropertyNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Required

True when the property is required, when creating new purchase invoice lines. False when this only suggests the usage of the property. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### ProductType

The [ProductType](General.Products.ProductTypePurchaseInvoiceLineProperties.md#producttype) to which this ProductTypePurchaseInvoiceLineProperty belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ProductTypes](General.Products.ProductTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Property

The user-defined property. It should be with Entity Type = 'Purchase Invoice Line'. [Required] [Filter(multi eq)]

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Products.ProductTypePurchaseInvoiceLineProperties erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductTypePurchaseInvoiceLineProperties erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductTypePurchaseInvoiceLineProperties?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductTypePurchaseInvoiceLineProperties?$top=10>

