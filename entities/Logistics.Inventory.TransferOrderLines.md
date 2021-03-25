---
uid: Logistics.Inventory.TransferOrderLines
---
# Logistics.Inventory.TransferOrderLines Entity

**Namespace:** [Logistics.Inventory](Logistics.Inventory.md)  

Details of Transfer Orders. Each line contains order for the movement of one product. Entity: Inv_Transfer_Order_Lines

## Default Visualization
Default Display Text Format:  
_{TransferOrder.DocumentType.Code}:{TransferOrder.DocumentNo}:{LineOrd} - {TransferOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_TransferOrder.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Inventory.TransferOrders](Logistics.Inventory.TransferOrders.md)  
Aggregate Root:  
[Logistics.Inventory.TransferOrders](Logistics.Inventory.TransferOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DueDateIn](Logistics.Inventory.TransferOrderLines.md#duedatein) | datetime | The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header. `Required` `Filter(ge;le)` 
| [DueDateOut](Logistics.Inventory.TransferOrderLines.md#duedateout) | datetime | When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header. `Required` `Filter(ge;le)` 
| [Id](Logistics.Inventory.TransferOrderLines.md#id) | guid |  
| [LineOrd](Logistics.Inventory.TransferOrderLines.md#lineord) | int32 | Line ordinal position within the transaction. Duplicates are allowed, but not advised. `Required` 
| [Notes](Logistics.Inventory.TransferOrderLines.md#notes) | string (254) __nullable__ | Notes for this TransferOrderLine. 
| [Quantity](Logistics.Inventory.TransferOrderLines.md#quantity) | [Quantity](../data-types.md#quantity) | Quantity ordered for transfer. `Unit: QuantityUnit` `Required` `Default(1)` `Filter(ge;le)` 
| [QuantityBase](Logistics.Inventory.TransferOrderLines.md#quantitybase) | [Quantity](../data-types.md#quantity) | Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Filter(ge;le)` 
| [StandardQuantityBase](Logistics.Inventory.TransferOrderLines.md#standardquantitybase) | [Quantity](../data-types.md#quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` `Introduced in version 18.2` 
| [StandardUnitPrice](Logistics.Inventory.TransferOrderLines.md#standardunitprice) | [Amount](../data-types.md#amount) __nullable__ | Standard unit price of the product during the creation of the transfer order line. `Currency: TransferOrder.DocumentCurrency` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Inventory.TransferOrderLines.md#document) | [TransferOrders](Logistics.Inventory.TransferOrders.md) | The parent transfer order. `Required` `Filter(multi eq)` |
| [FromStoreBin](Logistics.Inventory.TransferOrderLines.md#fromstorebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | From which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. `Filter(multi eq)` |
| [Lot](Logistics.Inventory.TransferOrderLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | If non-null, contains the specific lot to use for the movement. `Filter(multi eq)` |
| [Product](Logistics.Inventory.TransferOrderLines.md#product) | [Products](General.Products.Products.md) | The product which will be transferred. `Required` `Filter(multi eq)` |
| [ProductCode](Logistics.Inventory.TransferOrderLines.md#productcode) | [ProductCodes](General.Products.ProductCodes.md) (nullable) | Selects the product thru some of the product codes. `Filter(multi eq)` |
| [ProductVariant](Logistics.Inventory.TransferOrderLines.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | If specified determines which product variant of the current product in this line is used. `Filter(multi eq)` |
| [QuantityUnit](Logistics.Inventory.TransferOrderLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. `Required` `Filter(multi eq)` |
| [SerialNumber](Logistics.Inventory.TransferOrderLines.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | Which serial number to receive/issue. null means that serial number is unknown or not applicable. `Filter(multi eq)` |
| [ToStoreBin](Logistics.Inventory.TransferOrderLines.md#tostorebin) | [StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | To which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. `Filter(multi eq)` |
| [TransferOrder](Logistics.Inventory.TransferOrderLines.md#transferorder) | [TransferOrders](Logistics.Inventory.TransferOrders.md) | The parent transfer order. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DueDateIn

The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header. `Required` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransferOrder.DefaultDueDateIn`

_Front-End Recalc Expressions:_  
`obj.TransferOrder.DefaultDueDateIn`
### DueDateOut

When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header. `Required` `Filter(ge;le)`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`obj.TransferOrder.DefaultDueDateOut`

_Front-End Recalc Expressions:_  
`obj.TransferOrder.DefaultDueDateOut`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineOrd

Line ordinal position within the transaction. Duplicates are allowed, but not advised. `Required`

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.TransferOrder.Lines.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.TransferOrder.Lines.Select( c => c.LineOrd).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this TransferOrderLine.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Quantity

Quantity ordered for transfer. `Unit: QuantityUnit` `Required` `Default(1)` `Filter(ge;le)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### QuantityBase

Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `Filter(ge;le)`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. `Unit: Product.BaseMeasurementCategory.BaseUnit` `Required` `ReadOnly` `Introduced in version 18.2`

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Quantity == null) OrElse ( obj.QuantityUnit == null)) OrElse ( obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo( obj.Product.BaseUnit, obj.Product))`
### StandardUnitPrice

Standard unit price of the product during the creation of the transfer order line. `Currency: TransferOrder.DocumentCurrency`

_Type_: **[Amount](../data-types.md#amount) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF( ( ( obj.Product != null) AndAlso ( obj.QuantityUnit != null)), obj.Product.GetStandardUnitPrice( obj.QuantityUnit, obj.TransferOrder.ToStore.Currency, obj.TransferOrder.CurrencyDirectory), obj.StandardUnitPrice)`

## Reference Details

### Document

The parent transfer order. `Required` `Filter(multi eq)`

_Type_: **[TransferOrders](Logistics.Inventory.TransferOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### FromStoreBin

From which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. `Filter(multi eq)`

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

If non-null, contains the specific lot to use for the movement. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product which will be transferred. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.Product.IfNullThen( obj.Product)`
### ProductCode

Selects the product thru some of the product codes. `Filter(multi eq)`

_Type_: **[ProductCodes](General.Products.ProductCodes.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`IIF( ( ( ( obj.Product != null) AndAlso ( obj.ProductCode != null)) AndAlso ( obj.Product != obj.ProductCode.Product)), null, obj.ProductCode)`
### ProductVariant

If specified determines which product variant of the current product in this line is used. `Filter(multi eq)`

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

_Front-End Recalc Expressions:_  
`obj.ProductCode.CodingSystem.DefaultMeasurementUnit.IfNullThen( obj.Product.MeasurementUnit.IfNullThen( obj.QuantityUnit))`
### SerialNumber

Which serial number to receive/issue. null means that serial number is unknown or not applicable. `Filter(multi eq)`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToStoreBin

To which store bin to issue/receive the products. null means that the store bin is unknown or not applicable. `Filter(multi eq)`

_Type_: **[StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### TransferOrder

The parent transfer order. `Required` `Filter(multi eq)` `Owner`

_Type_: **[TransferOrders](Logistics.Inventory.TransferOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Inventory.TransferOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Inventory.TransferOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Inventory_TransferOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Inventory_TransferOrderLines?$top=10>

