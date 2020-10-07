# General.Products.ProductTypes

Categorization of the products by their nature. Entity: Gen_Product_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](General.Products.ProductTypes.md#Id) | guid |  
| [IsDefault](General.Products.ProductTypes.md#IsDefault) | boolean | When checked specifies that this type is set by default for new products unless another type is specified in the product groups. [Required] [Default(false)] [Filter(eq)] 
| [IsFixedAsset](General.Products.ProductTypes.md#IsFixedAsset) | boolean | True when assets are acquired or retired when products from this type are purchased or sold. [Required] [Default(false)] [Filter(eq)] 
| [IsServiceActivityService](General.Products.ProductTypes.md#IsServiceActivityService) | boolean | True when the product corresponds to service used in service documents (like service activities). [Required] [Default(false)] [Filter(eq)] 
| [IsServiced](General.Products.ProductTypes.md#IsServiced) | boolean | True when the products of this type create service agreements and can be serviced. [Required] [Default(false)] [Filter(eq)] 
| [IsShipped](General.Products.ProductTypes.md#IsShipped) | boolean | True when the products from this type are being shipped after sales. [Required] [Default(false)] [Filter(eq)] 
| [IsStocked](General.Products.ProductTypes.md#IsStocked) | boolean | True=The products of this type are stocked in a warehouse; false=otherwise (services). [Required] [Default(true)] [Filter(eq)] 
| [LotAutoCreation](General.Products.ProductTypes.md#LotAutoCreation) | boolean | If checked specifies that lots are automatically created by the receiving orders with which the products are received. [Required] [Default(false)] 
| [Code](General.Products.ProductTypes.md#Code) | string | The unique code of the ProductType. [Required] [Filter(eq)] 
| [Name](General.Products.ProductTypes.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this ProductType. [Required] [Filter(eq;like)] [ORD] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| PurchaseInvoiceLineProperties | [General.Products.ProductTypePurchaseInvoiceLineProperties](General.Products.ProductTypePurchaseInvoiceLineProperties.md) | List of [ProductTypePurchaseInvoiceLineProperty](General.Products.ProductTypePurchaseInvoiceLineProperties.md) child objects, based on the [General.Products.ProductTypePurchaseInvoiceLineProperty.ProductType](General.Products.ProductTypePurchaseInvoiceLineProperties.md#ProductType) back reference 
| TaxGroups | [Crm.Pos.ProductTypeTaxGroups](Crm.Pos.ProductTypeTaxGroups.md) | List of [ProductTypeTaxGroup](Crm.Pos.ProductTypeTaxGroups.md) child objects, based on the [Crm.Pos.ProductTypeTaxGroup.ProductType](Crm.Pos.ProductTypeTaxGroups.md#ProductType) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsDefault

> When checked specifies that this type is set by default for new products unless another type is specified in the product groups. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsFixedAsset

> True when assets are acquired or retired when products from this type are purchased or sold. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsServiceActivityService

> True when the product corresponds to service used in service documents (like service activities). [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsServiced

> True when the products of this type create service agreements and can be serviced. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsShipped

> True when the products from this type are being shipped after sales. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### IsStocked

> True=The products of this type are stocked in a warehouse; false=otherwise (services). [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LotAutoCreation

> If checked specifies that lots are automatically created by the receiving orders with which the products are received. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Code

> The unique code of the ProductType. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### Name

> The name of this ProductType. [Required] [Filter(eq;like)] [ORD]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  



## Business Rules

[!list erp.entity=General.Products.ProductTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Products.ProductTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Products.ProductTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Products_ProductTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Products_ProductTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Gen_Product_Types?$top=10>

