---
uid: Logistics.Inventory.TransferOrderLines
---
# Logistics.Inventory.TransferOrderLines

Details of Transfer Orders. Each line contains order for the movement of one product. Entity: Inv_Transfer_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Inventory.TransferOrderLines.md#Id) | guid |  
| [DueDateIn](Logistics.Inventory.TransferOrderLines.md#DueDateIn) | datetime | The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header. [Required] [Filter(ge;le)] 
| [DueDateOut](Logistics.Inventory.TransferOrderLines.md#DueDateOut) | datetime | When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header. [Required] [Filter(ge;le)] 
| [LineOrd](Logistics.Inventory.TransferOrderLines.md#LineOrd) | int32 | Line ordinal position within the transaction. Duplicates are allowed, but not advised. [Required] 
| [Notes](Logistics.Inventory.TransferOrderLines.md#Notes) | string (nullable) | Notes for this TransferOrderLine. 
| [Quantity](Logistics.Inventory.TransferOrderLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | Quantity ordered for transfer. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)] 
| [QuantityBase](Logistics.Inventory.TransferOrderLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Filter(ge;le)] 
| [StandardQuantityBase](Logistics.Inventory.TransferOrderLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [StandardUnitPrice](Logistics.Inventory.TransferOrderLines.md#StandardUnitPrice) | [Amount](../data-types.md#Amount) (nullable) | Standard unit price of the product during the creation of the transfer order line. [Currency: TransferOrder.DocumentCurrency] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FromStoreBin](Logistics.Inventory.TransferOrderLines.md#FromStoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | From which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. [Filter(multi eq)] |
| [Lot](Logistics.Inventory.TransferOrderLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | If non-null, contains the specific lot to use for the movement. [Filter(multi eq)] |
| [ProductCode](Logistics.Inventory.TransferOrderLines.md#ProductCode) | [General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable) | Selects the product thru some of the product codes. [Filter(multi eq)] |
| [Product](Logistics.Inventory.TransferOrderLines.md#Product) | [General.Products.Products](General.Products.Products.md) | The product which will be transferred. [Required] [Filter(multi eq)] |
| [ProductVariant](Logistics.Inventory.TransferOrderLines.md#ProductVariant) | [General.ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. [Filter(multi eq)] |
| [QuantityUnit](Logistics.Inventory.TransferOrderLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SerialNumber](Logistics.Inventory.TransferOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [ToStoreBin](Logistics.Inventory.TransferOrderLines.md#ToStoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | To which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. [Filter(multi eq)] |
| [TransferOrder](Logistics.Inventory.TransferOrderLines.md#TransferOrder) | [Logistics.Inventory.TransferOrders](Logistics.Inventory.TransferOrders.md) | The parent transfer order. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DueDateIn

> The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransferOrder.DefaultDueDateIn`

_Front-End Recalc Expressions:_  
`obj.TransferOrder.DefaultDueDateIn`
### DueDateOut

> When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransferOrder.DefaultDueDateOut`

_Front-End Recalc Expressions:_  
`obj.TransferOrder.DefaultDueDateOut`
### LineOrd

> Line ordinal position within the transaction. Duplicates are allowed, but not advised. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.TransferOrder.Lines.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.TransferOrder.Lines.Select(c => c.LineOrd).DefaultIfEmpty(0).Max() + 10)`
### Notes

> Notes for this TransferOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> Quantity ordered for transfer. [Unit: QuantityUnit] [Required] [Default(1)] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

> Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update. [Unit: Product.BaseMeasurementCategory.BaseUnit] [Required] [Filter(ge;le)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
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
### StandardUnitPrice

> Standard unit price of the product during the creation of the transfer order line. [Currency: TransferOrder.DocumentCurrency]

_Type_: **[Amount](../data-types.md#Amount) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(((obj.Product != null) AndAlso (obj.QuantityUnit != null)), obj.Product.GetStandardUnitPrice(obj.QuantityUnit, obj.TransferOrder.ToStore.Currency, obj.TransferOrder.CurrencyDirectory), obj.StandardUnitPrice)`

## Reference Details

### FromStoreBin

> From which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Lot

> If non-null, contains the specific lot to use for the movement. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProductCode

> Selects the product thru some of the product codes. [Filter(multi eq)]

_Type_: **[General.Products.ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF((((obj.Product != null) AndAlso (obj.ProductCode != null)) AndAlso (obj.Product != obj.ProductCode.Product)), null, obj.ProductCode)`
### Product

> The product which will be transferred. [Required] [Filter(multi eq)]

_Type_: **[General.Products.Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product.IfNullThen(obj.Product)`
### ProductVariant

> If specified determines which product variant of the current product in this line is used. [Filter(multi eq)]

_Type_: **[General.ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen(obj.Product.MeasurementUnit.IfNullThen(obj.QuantityUnit))`
### SerialNumber

> Which serial number to receive/issue. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ToStoreBin

> To which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TransferOrder

> The parent transfer order. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Inventory.TransferOrders](Logistics.Inventory.TransferOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Inventory.TransferOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.TransferOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Inventory.TransferOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_TransferOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_TransferOrderLines?$top=10>

