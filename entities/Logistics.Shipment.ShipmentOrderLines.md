---
uid: Logistics.Shipment.ShipmentOrderLines
---
# Logistics.Shipment.ShipmentOrderLines

Represents detail lines of orders for shipment of sales orders to customers. Each line orders the shipment of one product. Entity: Log_Shipment_Order_Lines

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Shipment.ShipmentOrderLines.md#Id) | guid |  
| [BoxCount](Logistics.Shipment.ShipmentOrderLines.md#BoxCount) | int32 (nullable) | The count of boxes in which the goods are packaged. null means unknown. 
| [Finished](Logistics.Shipment.ShipmentOrderLines.md#Finished) | boolean | True if this shipment should prohibit further shipments for the sales order line. [Required] [Default(false)] [Filter(eq)] 
| [GrossWeightkg](Logistics.Shipment.ShipmentOrderLines.md#GrossWeightkg) | decimal (nullable) | The gross weight of the whole line in kilogramms. null means unknown. 
| [GuaranteePeriodDays](Logistics.Shipment.ShipmentOrderLines.md#GuaranteePeriodDays) | int32 (nullable) | Guarantee period in days for the offered product. null for non-serviced products. 
| [Heightm](Logistics.Shipment.ShipmentOrderLines.md#Heightm) | decimal (nullable) | The height of the package in meters. null means unknown. 
| [Lengthm](Logistics.Shipment.ShipmentOrderLines.md#Lengthm) | decimal (nullable) | The length of the package in meters. null means unknown. 
| [LineNo](Logistics.Shipment.ShipmentOrderLines.md#LineNo) | int32 | Line number, unique for the shipment. [Required] 
| [NetWeightkg](Logistics.Shipment.ShipmentOrderLines.md#NetWeightkg) | decimal (nullable) | The net weight of the entire batch of goods in kilograms. null means unknown. 
| [Notes](Logistics.Shipment.ShipmentOrderLines.md#Notes) | string (nullable) | Specific notes for this line. 
| [PalletNo](Logistics.Shipment.ShipmentOrderLines.md#PalletNo) | int32 (nullable) | The number of the pallet in which the goods are packaged. null means unknown. 
| [ParentLineNo](Logistics.Shipment.ShipmentOrderLines.md#ParentLineNo) | int32 (nullable) | The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line. 
| [PersistLot](Logistics.Shipment.ShipmentOrderLines.md#PersistLot) | boolean | If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. [Required] [Default(false)] [Filter(eq)] 
| [Quantity](Logistics.Shipment.ShipmentOrderLines.md#Quantity) | [Quantity](../data-types.md#Quantity) | The quantity to be shipped. [Unit: QuantityUnit] [Required] [Default(1)] 
| [QuantityBase](Logistics.Shipment.ShipmentOrderLines.md#QuantityBase) | [Quantity](../data-types.md#Quantity) | The equivalence of Quantity in the base measurement category of the product. [Unit: ParentSalesOrderLine.Product.BaseMeasurementCategory.BaseUnit] [Required] 
| [StandardQuantityBase](Logistics.Shipment.ShipmentOrderLines.md#StandardQuantityBase) | [Quantity](../data-types.md#Quantity) | The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: ParentSalesOrderLine.Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0) 
| [Volumel](Logistics.Shipment.ShipmentOrderLines.md#Volumel) | decimal (nullable) | The volume in litres of the whole batch. null means unknown. 
| [Widthm](Logistics.Shipment.ShipmentOrderLines.md#Widthm) | decimal (nullable) | The width of the package in meters. null means unknown. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Lot](Logistics.Shipment.ShipmentOrderLines.md#Lot) | [Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable) | The store lot from which to take the goods. [Filter(multi eq)] |
| [ParentDocument](Logistics.Shipment.ShipmentOrderLines.md#ParentDocument) | [General.Documents](General.Documents.md) (nullable) | The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)] |
| [ParentSalesOrderLine](Logistics.Shipment.ShipmentOrderLines.md#ParentSalesOrderLine) | [Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md) | Sales order line which is shipped. [Required] [Filter(multi eq)] |
| [QuantityUnit](Logistics.Shipment.ShipmentOrderLines.md#QuantityUnit) | [General.MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SerialNumber](Logistics.Shipment.ShipmentOrderLines.md#SerialNumber) | [Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The serial number of the shipped product. null means that serial number is unknown or not applicable. [Filter(multi eq)] |
| [ShipmentOrder](Logistics.Shipment.ShipmentOrderLines.md#ShipmentOrder) | [Logistics.Shipment.ShipmentOrders](Logistics.Shipment.ShipmentOrders.md) | The [ShipmentOrder](Logistics.Shipment.ShipmentOrderLines.md#ShipmentOrder) to which this ShipmentOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [StoreBin](Logistics.Shipment.ShipmentOrderLines.md#StoreBin) | [Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable) | The store bin from which to take the goods. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BoxCount

> The count of boxes in which the goods are packaged. null means unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Finished

> True if this shipment should prohibit further shipments for the sales order line. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### GrossWeightkg

> The gross weight of the whole line in kilogramms. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### GuaranteePeriodDays

> Guarantee period in days for the offered product. null for non-serviced products.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`IIF(obj.ParentSalesOrderLine.Product.ProductType.IsServiced, obj.ParentSalesOrderLine.Product.GuaranteePeriodDays, null)`
### Heightm

> The height of the package in meters. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Lengthm

> The length of the package in meters. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LineNo

> Line number, unique for the shipment. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`(obj.ShipmentOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`

_Front-End Recalc Expressions:_  
`(obj.ShipmentOrder.Lines.Select(c => c.LineNo).DefaultIfEmpty(0).Max() + 10)`
### NetWeightkg

> The net weight of the entire batch of goods in kilograms. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Specific notes for this line.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PalletNo

> The number of the pallet in which the goods are packaged. null means unknown.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentLineNo

> The number of the line within the parent document, which the current line executes. null when the current line does not execute parent line.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PersistLot

> If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Quantity

> The quantity to be shipped. [Unit: QuantityUnit] [Required] [Default(1)]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

_Front-End Recalc Expressions:_  
`new Quantity(obj.ParentSalesOrderLine.Quantity.Value, obj.QuantityUnit)`
### QuantityBase

> The equivalence of Quantity in the base measurement category of the product. [Unit: ParentSalesOrderLine.Product.BaseMeasurementCategory.BaseUnit] [Required]

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.QuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### StandardQuantityBase

> The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution. [Unit: ParentSalesOrderLine.Product.BaseMeasurementCategory.BaseUnit] [Required] [ReadOnly] (Introduced in version 18.2.100.0)

_Type_: **[Quantity](../data-types.md#Quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, IIF(obj.Product.AllowVariableMeasurementRatios, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product), obj.QuantityBase))`

_Front-End Recalc Expressions:_  
`IIF((((obj.Quantity == null) OrElse (obj.QuantityUnit == null)) OrElse (obj.Product == null)), obj.StandardQuantityBase, obj.Quantity.ConvertTo(obj.Product.BaseUnit, obj.Product))`
### Volumel

> The volume in litres of the whole batch. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Widthm

> The width of the package in meters. null means unknown.

_Type_: **decimal (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Lot

> The store lot from which to take the goods. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ParentSalesOrderLine.Lot`
### ParentDocument

> The document, which the current line executes. null when the current line does not execute another line. [Filter(multi eq)]

_Type_: **[General.Documents](General.Documents.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ParentSalesOrderLine

> Sales order line which is shipped. [Required] [Filter(multi eq)]

_Type_: **[Crm.Sales.SalesOrderLines](Crm.Sales.SalesOrderLines.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[General.MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

_Front-End Recalc Expressions:_  
`obj.ParentSalesOrderLine.QuantityUnit`
### SerialNumber

> The serial number of the shipped product. null means that serial number is unknown or not applicable. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ShipmentOrder

> The [ShipmentOrder](Logistics.Shipment.ShipmentOrderLines.md#ShipmentOrder) to which this ShipmentOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Logistics.Shipment.ShipmentOrders](Logistics.Shipment.ShipmentOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### StoreBin

> The store bin from which to take the goods. [Filter(multi eq)]

_Type_: **[Logistics.Inventory.StoreBins](Logistics.Inventory.StoreBins.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Shipment.ShipmentOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Shipment.ShipmentOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Shipment.ShipmentOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Shipment_ShipmentOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Shipment_ShipmentOrderLines?$top=10>

