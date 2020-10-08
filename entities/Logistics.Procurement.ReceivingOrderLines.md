---
uid: Logistics.Procurement.ReceivingOrderLines
---
# Logistics.Procurement.ReceivingOrderLines

Contains detail records of Receiving Orders. Each line contains the receiving of a quantity of a product. Entity: Scm_Receiving_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Procurement.ReceivingOrderLines.md#Id) | guid |  
| [ConfirmedQuantity](Logistics.Procurement.ReceivingOrderLines.md#ConfirmedQuantity) | [Quantity](../data-types.md#Quantity) (nullable) | The final confirmed received quantity, after adjustments. It is used in all calculations for the order. Usually changed with adjustments to the receivemnt order, in regard to the warehouse receipt or the invoice. When null, its value is equal to Quantity. [Unit: QuantityUnit] 
| [ConfirmedQuantityBase](Logistics.Procurement.ReceivingOrderLines.md#ConfirmedQuantityBase) | [Quantity](../data-types.md#Quantity) (nullable) | The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] 
| [ConfirmedStandardQuantityBase](Logistics.Procurement.ReceivingOrderLines.md#ConfirmedStandardQuantityBase) | [Quantity](../data-types.md#Quantity) (nullable) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Confirmed Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [ReadOnly] (Introduced in version 18.2.100.0) 
| [Finished](Logistics.Procurement.ReceivingOrderLines.md#Finished) | boolean | When true, denotes that this is the last receivement for this purchase order line and further receivements are not expected. [Required] [Default(false)] 
| [LineAmount](Logistics.Procurement.ReceivingOrderLines.md#LineAmount) | [Amount](../data-types.md#Amount) | The total amount for the line. Equals to Quantity * Price_Per_Unit. [Currency: ReceivingOrder.DocumentCurrency] [Required] [Default(0)] 
| [LineNo](Logistics.Procurement.ReceivingOrderLines.md#LineNo) | int32 | Line number, unique within the ReceivingOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the ReceivingOrder (in order to allow insertions with adjustment documents). [Required] 
| [Notes](Logistics.Procurement.ReceivingOrderLines.md#Notes) | string (nullable) | Notes for this ReceivingOrderLine. 
| [PricePerUnit](Logistics.Procurement.ReceivingOrderLines.md#PricePerUnit) | [Amount](../data-types.md#Amount) | The unit price of the received products, in the documents currency. [Currency: ReceivingOrder.DocumentCurrency] [Required] [Default(0)] 
| [ProductDescription](Logistics.Procurement.ReceivingOrderLines.md#ProductDescription) | [MultilanguageString](../data-types.md#MultilanguageString) | The name of the received product, initially copied from the name in the product definition. The field can be edited by the user. [Required] 
| [Quantity](Logistics.Procurement.ReceivingOrderLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | The received quantity. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityBase](Logistics.Procurement.ReceivingOrderLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | The equivalence of Quantity, in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [StandardQuantityBase](Logistics.Procurement.ReceivingOrderLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LineStore](Logistics.Procurement.ReceivingOrderLines.md#LineStore) | [Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable) | The store in which the goods are received. [Filter(multi eq)] |
| [Lot](Logistics.Procurement.ReceivingOrderLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The lot of the received goods. [Filter(multi eq)] |
| [ProductCode](Logistics.Procurement.ReceivingOrderLines.md#ProductCode) | [General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable) | When not null, specifies that the product was selected using the specified product code record. [Filter(multi eq)] |
| [Product](Logistics.Procurement.ReceivingOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The received product. [Required] [Filter(multi eq)] |
| [ProductVariant](Logistics.Procurement.ReceivingOrderLines.md#ProductVariant) | [General.ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [PurchaseOrderLine](Logistics.Procurement.ReceivingOrderLines.md#PurchaseOrderLine) | [Logistics.Procurement.PurchaseOrderLines](Logistics.Procurement.PurchaseOrderLines.md) (nullable) | The purchase order line for which we are receiving quantity. [Filter(multi eq)] |
| [PurchaseProductPrice](Logistics.Procurement.ReceivingOrderLines.md#PurchaseProductPrice) | [Logistics.Procurement.PurchaseProductPrices](Logistics.Procurement.PurchaseProductPrices.md) (nullable) | When not null, specifies that the purchase unit price is loaded automatically from the specified purchase price record. [Filter(multi eq)] |
| [QuantityUnit](Logistics.Procurement.ReceivingOrderLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. Initially copied from the Default Measurement Unit of the Product. [Required] [Filter(multi eq)] |
| [ReceivingOrder](Logistics.Procurement.ReceivingOrderLines.md#ReceivingOrder) | [Logistics.Procurement.ReceivingOrders](Logistics.Procurement.ReceivingOrders.md) | The [ReceivingOrder](Logistics.Procurement.ReceivingOrderLines.md#ReceivingOrder) to which this ReceivingOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [SerialNumber](Logistics.Procurement.ReceivingOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [StoreBin](Logistics.Procurement.ReceivingOrderLines.md#StoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | The store bin in which to receive the goods. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ConfirmedQuantity

> The final confirmed received quantity, after adjustments. It is used in all calculations for the order. Usually changed with adjustments to the receivemnt order, in regard to the warehouse receipt or the invoice. When null, its value is equal to Quantity. [Unit: QuantityUnit]

_Type_: **[Quantity](../data-types.md#Quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ConfirmedQuantityBase

> The theoretical equivalence of Confirmed Quantity in base measurement unit according to the current measurement dimensions of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit]

_Type_: **[Quantity](../data-types.md#Quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((((obj.ConfirmedQuantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.ConfirmedQuantityBase, obj.ConfirmedQuantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### ConfirmedStandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. null means to convert the value from Confirmed Quantity using the measurement ratios. [Unit: Product.BaseMeasurementCategory.BaseUnit] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((((obj.ConfirmedQuantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.ConfirmedStandardQuantityBase, obj.ConfirmedQuantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### Finished

> When true, denotes that this is the last receivement for this purchase order line and further receivements are not expected. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LineAmount

> The total amount for the line. Equals to Quantity * Price_Per_Unit. [Currency: ReceivingOrder.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Back-End Default Expression:_  
`IIF((((obj.ConfirmedQuantity ?? obj.Quantity) == null) OrElse (obj.PricePerUnit == null)), obj.LineAmount, ((obj.ConfirmedQuantity ?? obj.Quantity).Value * obj.PricePerUnit).Round())`

_Front-End Recalc Expressions:_  
`IIF((((obj.ConfirmedQuantity ?? obj.Quantity) == null) OrElse (obj.PricePerUnit == null)), obj.LineAmount, ((obj.ConfirmedQuantity ?? obj.Quantity).Value * obj.PricePerUnit).Round())`
### LineNo

> Line number, unique within the ReceivingOrder. Usually is increasing number like 10, 20, 30, ... when initially entering the ReceivingOrder (in order to allow insertions with adjustment documents). [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ReceivingOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ReceivingOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this ReceivingOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PricePerUnit

> The unit price of the received products, in the documents currency. [Currency: ReceivingOrder.DocumentCurrency] [Required] [Default(0)]

_Type_: **[Amount](../data-types.md#Amount)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`obj.GetPurchasePriceFromPurchasePriceList(obj.PurchaseProductPrice, obj.QuantityUnit)`
### ProductDescription

> The name of the received product, initially copied from the name in the product definition. The field can be edited by the user. [Required]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.Product.Name`

_Front-End Recalc Expressions:_  
`obj.Product.Name`
### Quantity

> The received quantity. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> The equivalence of Quantity, in the base measurement category of the product. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

## Reference Details

### LineStore

> The store in which the goods are received. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Stores](Logistics.Inventory.Stores.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ReceivingOrder.Store`

_Front-End Recalc Expressions:_  
`obj.ReceivingOrder.Store`
### Lot

> The lot of the received goods. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductCode

> When not null, specifies that the product was selected using the specified product code record. [Filter(multi eq)]

_Type_: **[General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Product

> The received product. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductVariant

> If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[General.ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseOrderLine

> The purchase order line for which we are receiving quantity. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseOrderLines](Logistics.Procurement.PurchaseOrderLines.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PurchaseProductPrice

> When not null, specifies that the purchase unit price is loaded automatically from the specified purchase price record. [Filter(multi eq)]

_Type_: **[Logistics.Procurement.PurchaseProductPrices](Logistics.Procurement.PurchaseProductPrices.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.DeterminePurchaseProductPrice(Convert(obj.ReceivingOrder.DocumentDate, Nullable`1), obj.ReceivingOrder.Supplier, obj.Product, (obj.ConfirmedQuantity ?? obj.Quantity), obj.ReceivingOrder.EnterpriseCompany, obj.ReceivingOrder.PurchasePriceList)`
### QuantityUnit

> The measurement unit of Quantity. Initially copied from the Default Measurement Unit of the Product. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Product.PurchaseMeasurementUnit).IfNullThen(obj.Product.MeasurementUnit).IfNullThen(obj.QuantityUnit)`

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Product.PurchaseMeasurementUnit).IfNullThen(obj.Product.MeasurementUnit).IfNullThen(obj.QuantityUnit)`
### ReceivingOrder

> The [ReceivingOrder](Logistics.Procurement.ReceivingOrderLines.md#ReceivingOrder) to which this ReceivingOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Procurement.ReceivingOrders](Logistics.Procurement.ReceivingOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SerialNumber

> Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreBin

> The store bin in which to receive the goods. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Procurement.ReceivingOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Procurement.ReceivingOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Procurement.ReceivingOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Procurement_ReceivingOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Procurement_ReceivingOrderLines?$top=10>

