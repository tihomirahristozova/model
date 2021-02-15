---
uid: Logistics.Procurement.PurchaseOrderLines
---
# Logistics.Procurement.PurchaseOrderLines Entity

Contains detail lines of purchase orders. Entity: Scm_Purchase_Order_Lines

Default Display Text Format:  
_{PurchaseOrder.DocumentType.Code}:{PurchaseOrder.DocumentNo}:{LineNo} - {PurchaseOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_PurchaseOrder.DocumentNo_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConfirmedPricePerUnit](Logistics.Procurement.PurchaseOrderLines.md#confirmedpriceperunit) | [Amount](../data-types.md#amount) (nullable) | The unit price that is confirmed by the supplier. null if there was no order confirmation. [Currency: PurchaseOrder.DocumentCurrency] 
| [ConfirmedQuantity](Logistics.Procurement.PurchaseOrderLines.md#confirmedquantity) | [Quantity](../data-types.md#quantity) (nullable) | The quantity that is confirmed by the supplier. null if there was no order confirmation. [Unit: QuantityUnit] [Filter(ge;le)] 
| [ConfirmedQuantityBase](Logistics.Procurement.PurchaseOrderLines.md#confirmedquantitybase) | [Quantity](../data-types.md#quantity) (nullable) | The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [ReadOnly] 
| [ConfirmedStandard<br />QuantityBase](Logistics.Procurement.PurchaseOrderLines.md#confirmedstandardquantitybase) | [Quantity](../data-types.md#quantity) (nullable) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Confirmed Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [ReadOnly] [Introduced in version 18.2] 
| [Id](Logistics.Procurement.PurchaseOrderLines.md#id) | guid |  
| [LineNo](Logistics.Procurement.PurchaseOrderLines.md#lineno) | int32 | Line number, unique within the PurchaseOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the PurchaseOrder (in order to allow insertions with adjustment documents). [Required] 
| [Notes](Logistics.Procurement.PurchaseOrderLines.md#notes) | string (nullable) | Notes for this PurchaseOrderLine. 
| [ParentLineNo](Logistics.Procurement.PurchaseOrderLines.md#parentlineno) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute line. [Filter(eq)] [Introduced in version 18.2] 
| [PlannedDeliveryDate](Logistics.Procurement.PurchaseOrderLines.md#planneddeliverydate) | datetime | The planned delivery date for this line. [Required] [Filter(ge;le)] 
| [PricePerUnit](Logistics.Procurement.PurchaseOrderLines.md#priceperunit) | [Amount](../data-types.md#amount) (nullable) | The expected unit price of the ordered products, in the document currency. [Currency: PurchaseOrder.DocumentCurrency] 
| [ProductDescription](Logistics.Procurement.PurchaseOrderLines.md#productdescription) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user. [Required] [Filter(like)] 
| [Quantity](Logistics.Procurement.PurchaseOrderLines.md#quantity) | [Quantity](../data-types.md#quantity) | The quantity ordered. [Unit: QuantityUnit] [Required] [Default(0)] [Filter(ge;le)] 
| [QuantityBase](Logistics.Procurement.PurchaseOrderLines.md#quantitybase) | [Quantity](../data-types.md#quantity) | The equivalence of Quantity, in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly] 
| [StandardQuantityBase](Logistics.Procurement.PurchaseOrderLines.md#standardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Procurement.PurchaseOrderLines.md#document) | [PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) | The [PurchaseOrder](Logistics.Procurement.PurchaseOrderLines.md#purchaseorder) to which this PurchaseOrderLine belongs. [Required] [Filter(multi eq)] |
| [Lot](Logistics.Procurement.PurchaseOrderLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | When not null, indicates that a specific lot is required to be delivered. [Filter(multi eq)] |
| [ParentDocument](Logistics.Procurement.PurchaseOrderLines.md#parentdocument) | [Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] [Introduced in version 18.2] |
| [Product](Logistics.Procurement.PurchaseOrderLines.md#product) | [Products](General.Products.Products.md) | The ordered product. [Required] [Filter(multi eq)] |
| [ProductCode](Logistics.Procurement.PurchaseOrderLines.md#productcode) | [ProductCodes](General.Products.ProductCodes.md) (nullable) | When not null, specifies that the product was selected using the specified product code record. [Filter(multi eq)] |
| [ProductVariant](Logistics.Procurement.PurchaseOrderLines.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [PurchaseOrder](Logistics.Procurement.PurchaseOrderLines.md#purchaseorder) | [PurchaseOrders](Logistics.Procurement.PurchaseOrders.md) | The [PurchaseOrder](Logistics.Procurement.PurchaseOrderLines.md#purchaseorder) to which this PurchaseOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [PurchaseProductPrice](Logistics.Procurement.PurchaseOrderLines.md#purchaseproductprice) | [PurchaseProductPrices](Logistics.Procurement.PurchaseProductPrices.md) (nullable) | When not null, specifies that the purchase unit price is loaded automatically from the specified purchase price record. [Filter(multi eq)] |
| [QuantityUnit](Logistics.Procurement.PurchaseOrderLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [RequisitionLine](Logistics.Procurement.PurchaseOrderLines.md#requisitionline) | [RequisitionLines](Logistics.Procurement.RequisitionLines.md) (nullable) | When not null, specifies that the current line is based on the specified requisition line. [Filter(multi eq)] |


## Attribute Details

### ConfirmedPricePerUnit

The unit price that is confirmed by the supplier. null if there was no order confirmation. [Currency: PurchaseOrder.DocumentCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConfirmedQuantity

The quantity that is confirmed by the supplier. null if there was no order confirmation. [Unit: QuantityUnit] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ConfirmedQuantityBase

The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.ConfirmedQuantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.ConfirmedQuantityBase, obj.ConfirmedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### ConfirmedStandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Confirmed Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [ReadOnly] [Introduced in version 18.2]

_Type_: **[Quantity](../data-types.md#quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.ConfirmedQuantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.ConfirmedStandardQuantityBase, obj.ConfirmedQuantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Line number, unique within the PurchaseOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the PurchaseOrder (in order to allow insertions with adjustment documents). [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.PurchaseOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.PurchaseOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this PurchaseOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

The number of the line within the parent document, which the current line executes. null when the current line does not execute line. [Filter(eq)] [Introduced in version 18.2]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### PlannedDeliveryDate

The planned delivery date for this line. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.PurchaseOrder.PlannedDeliveryDate`

_Front-End Recalc Expressions:_  
`obj.PurchaseOrder.PlannedDeliveryDate`
### PricePerUnit

The expected unit price of the ordered products, in the document currency. [Currency: PurchaseOrder.DocumentCurrency]

_Type_: **[Amount](../data-types.md#amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.GetPurchasePriceForProductPriceUnit( obj.PurchaseProductPrice, obj.QuantityUnit)`
### ProductDescription

The name of the ordered product, initially copied from the name in the product definition. The field can be edited by the user. [Required] [Filter(like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.Name`

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

The quantity ordered. [Unit: QuantityUnit] [Required] [Default(0)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

The equivalence of Quantity, in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Default(0)] [ReadOnly]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] [Introduced in version 18.2]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

## Reference Details

### Document

The [PurchaseOrder](Logistics.Procurement.PurchaseOrderLines.md#purchaseorder) to which this PurchaseOrderLine belongs. [Required] [Filter(multi eq)]

_Type_: **[PurchaseOrders](Logistics.Procurement.PurchaseOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

When not null, indicates that a specific lot is required to be delivered. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ParentDocument

The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] [Introduced in version 18.2]

_Type_: **[Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The ordered product. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product`
### ProductCode

When not null, specifies that the product was selected using the specified product code record. [Filter(multi eq)]

_Type_: **[ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.ProductCode != null) AndAlso ( obj.Product != obj.ProductCode.Product)), null, obj.ProductCode)`
### ProductVariant

If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseOrder

The [PurchaseOrder](Logistics.Procurement.PurchaseOrderLines.md#purchaseorder) to which this PurchaseOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[PurchaseOrders](Logistics.Procurement.PurchaseOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### PurchaseProductPrice

When not null, specifies that the purchase unit price is loaded automatically from the specified purchase price record. [Filter(multi eq)]

_Type_: **[PurchaseProductPrices](Logistics.Procurement.PurchaseProductPrices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.DeterminePurchaseProductPrice( Convert( obj.Document.DocumentDate, Nullable`1), obj.PurchaseOrder.Supplier, obj.Product, obj.Quantity, obj.Document.EnterpriseCompany, obj.PurchaseOrder.PurchasePriceList)`
### QuantityUnit

The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen( obj.Product.PurchaseMeasurementUnit).IfNullThen( obj.Product.MeasurementUnit).IfNullThen( obj.QuantityUnit)`
### RequisitionLine

When not null, specifies that the current line is based on the specified requisition line. [Filter(multi eq)]

_Type_: **[RequisitionLines](Logistics.Procurement.RequisitionLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.PurchaseOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_PurchaseOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_PurchaseOrderLines?$top=10>

