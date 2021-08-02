---
uid: Logistics.Wms.WarehouseOrderLines
---
# Logistics.Wms.WarehouseOrderLines Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

A planned task (operation) in a warehouse order. Entity: Wms_Warehouse_Order_Lines (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{WarehouseOrder.DocumentType.Code}:{WarehouseOrder.DocumentNo}:{LineNo} - {WarehouseOrder.DocumentType.TypeName:T}_  
Default Search Member:  
_WarehouseOrder.DocumentNo_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Wms.WarehouseOrders](Logistics.Wms.WarehouseOrders.md)  
Aggregate Root:  
[Logistics.Wms.WarehouseOrders](Logistics.Wms.WarehouseOrders.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseOrderLines.md#id) | guid |  
| [LineNo](Logistics.Wms.WarehouseOrderLines.md#lineno) | int32 | Unique consecutive line number within the order. `Required` `Filter(eq)` 
| [Notes](Logistics.Wms.WarehouseOrderLines.md#notes) | string (max) __nullable__ | Notes for this WarehouseOrderLine. 
| [Quantity](Logistics.Wms.WarehouseOrderLines.md#quantity) | [Quantity (12, 3)](../data-types.md#quantity) | The quantity of the product, which should be processed. `Unit: QuantityUnit` `Required` `Default(0)` `Filter(eq;ge;le)` 
| [TaskType](Logistics.Wms.WarehouseOrderLines.md#tasktype) | [TaskType](Logistics.Wms.WarehouseOrderLines.md#tasktype) | The type of the task (operation), which should be performed. REC=Receive; DES=Despatch; MOV=Move; LBL=Label; INS=Inspect; PCK=Pack; UPK=Unpack; KIT=Assemble kit; RKT=Reverse kitting; CNT=Count; TSK=Task. `Required` `Filter(multi eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Wms.WarehouseOrderLines.md#document) | [WarehouseOrders](Logistics.Wms.WarehouseOrders.md) | The `WarehouseOrder`(Logistics.Wms.WarehouseOrderLines.md#warehouseorder) to which this WarehouseOrderLine belongs. `Required` `Filter(multi eq)` |
| [LogisticUnit](Logistics.Wms.WarehouseOrderLines.md#logisticunit) | [LogisticUnits](Logistics.LogisticUnits.md) (nullable) | Logistic unit, which should be used in the operation. `Filter(multi eq)` `Introduced in version 21.1.1.18` |
| [Lot](Logistics.Wms.WarehouseOrderLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot of the product, which should be used. null for operations, which are not lot-specific, or when any lot can be used. `Filter(multi eq)` |
| [Product](Logistics.Wms.WarehouseOrderLines.md#product) | [Products](General.Products.Products.md) (nullable) | The product, which should be used for the operation. `Filter(multi eq)` |
| [ProductVariant](Logistics.Wms.WarehouseOrderLines.md#productvariant) | [ProductVariants](General.ProductVariants.md) (nullable) | The product variant, which should be used. `Filter(multi eq)` `Introduced in version 21.1.1.18` |
| [QuantityUnit](Logistics.Wms.WarehouseOrderLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | The measurement unit of Quantity. null for operations, which are not quantity-related. `Filter(multi eq)` |
| [SerialNumber](Logistics.Wms.WarehouseOrderLines.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The serial number of the product, which should be used. null for operations, which are not serial number-specific, or when any serial number can be used. `Filter(multi eq)` |
| [ToWarehouseLocation](Logistics.Wms.WarehouseOrderLines.md#towarehouselocation) | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable) | Destination warehouse location. null for operations, which do not specify destination location. `Filter(multi eq)` |
| [WarehouseLocation](Logistics.Wms.WarehouseOrderLines.md#warehouselocation) | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable) | Location, where the opeartion should be performed. null for operations, which do not require location. `Filter(multi eq)` |
| [WarehouseOrder](Logistics.Wms.WarehouseOrderLines.md#warehouseorder) | [WarehouseOrders](Logistics.Wms.WarehouseOrders.md) | The `WarehouseOrder`(Logistics.Wms.WarehouseOrderLines.md#warehouseorder) to which this WarehouseOrderLine belongs. `Required` `Filter(multi eq)` `Owner` |
| [WarehouseWorker](Logistics.Wms.WarehouseOrderLines.md#warehouseworker) | [WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) (nullable) | Human or robot worker, which should execute the operation. null means that the line is shared among all workers, assigned to the order. `Filter(multi eq)` |
| [WarehouseZone](Logistics.Wms.WarehouseOrderLines.md#warehousezone) | [WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable) | The warehouse zone, in which the operation should be performed. null for operations which do not require specific zone. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

Unique consecutive line number within the order. `Required` `Filter(eq)`

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.WarehouseOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.WarehouseOrder.Lines.Select( c => c.LineNo).DefaultIfEmpty( 0).Max( ) + 10)`
### Notes

Notes for this WarehouseOrderLine.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### Quantity

The quantity of the product, which should be processed. `Unit: QuantityUnit` `Required` `Default(0)` `Filter(eq;ge;le)`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **Constant**  

### TaskType

The type of the task (operation), which should be performed. REC=Receive; DES=Despatch; MOV=Move; LBL=Label; INS=Inspect; PCK=Pack; UPK=Unpack; KIT=Assemble kit; RKT=Reverse kitting; CNT=Count; TSK=Task. `Required` `Filter(multi eq)`

_Type_: **[TaskType](Logistics.Wms.WarehouseOrderLines.md#tasktype)**  
Allowed values for the `TaskType`(Logistics.Wms.WarehouseOrderLines.md#tasktype) data attribute  
_Allowed Values (Logistics.Wms.WarehouseOrderLinesRepository.TaskType Enum Members)_  

| Value | Description |
| ---- | --- |
| Receive | Receive value. Stored as 'REC'. <br /> _Database Value:_ 'REC' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Receive' |
| Despatch | Despatch value. Stored as 'DES'. <br /> _Database Value:_ 'DES' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Despatch' |
| Move | Move value. Stored as 'MOV'. <br /> _Database Value:_ 'MOV' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Move' |
| Label | Label value. Stored as 'LBL'. <br /> _Database Value:_ 'LBL' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Label' |
| Inspect | Inspect value. Stored as 'INS'. <br /> _Database Value:_ 'INS' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Inspect' |
| Pack | Pack value. Stored as 'PCK'. <br /> _Database Value:_ 'PCK' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Pack' |
| Unpack | Unpack value. Stored as 'UPK'. <br /> _Database Value:_ 'UPK' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'Unpack' |
| AssembleKit | AssembleKit value. Stored as 'KIT'. <br /> _Database Value:_ 'KIT' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'AssembleKit' |
| ReverseKitting | ReverseKitting value. Stored as 'RKT'. <br /> _Database Value:_ 'RKT' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'ReverseKitting' |
| Count | Count value. Stored as 'CNT'. <br /> _Database Value:_ 'CNT' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'Count' |
| Task | Task value. Stored as 'TSK'. <br /> _Database Value:_ 'TSK' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'Task' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### Document

The `WarehouseOrder`(Logistics.Wms.WarehouseOrderLines.md#warehouseorder) to which this WarehouseOrderLine belongs. `Required` `Filter(multi eq)`

_Type_: **[WarehouseOrders](Logistics.Wms.WarehouseOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### LogisticUnit

Logistic unit, which should be used in the operation. `Filter(multi eq)` `Introduced in version 21.1.1.18`

_Type_: **[LogisticUnits](Logistics.LogisticUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Lot

The lot of the product, which should be used. null for operations, which are not lot-specific, or when any lot can be used. `Filter(multi eq)`

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The product, which should be used for the operation. `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ProductVariant

The product variant, which should be used. `Filter(multi eq)` `Introduced in version 21.1.1.18`

_Type_: **[ProductVariants](General.ProductVariants.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

The measurement unit of Quantity. null for operations, which are not quantity-related. `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

The serial number of the product, which should be used. null for operations, which are not serial number-specific, or when any serial number can be used. `Filter(multi eq)`

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToWarehouseLocation

Destination warehouse location. null for operations, which do not specify destination location. `Filter(multi eq)`

_Type_: **[WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseLocation

Location, where the opeartion should be performed. null for operations, which do not require location. `Filter(multi eq)`

_Type_: **[WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrder

The `WarehouseOrder`(Logistics.Wms.WarehouseOrderLines.md#warehouseorder) to which this WarehouseOrderLine belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[WarehouseOrders](Logistics.Wms.WarehouseOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### WarehouseWorker

Human or robot worker, which should execute the operation. null means that the line is shared among all workers, assigned to the order. `Filter(multi eq)`

_Type_: **[WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseZone

The warehouse zone, in which the operation should be performed. null for operations which do not require specific zone. `Filter(multi eq)`

_Type_: **[WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseOrderLines erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseOrderLines?$top=10>

