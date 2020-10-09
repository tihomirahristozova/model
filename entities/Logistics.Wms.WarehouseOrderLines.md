---
uid: Logistics.Wms.WarehouseOrderLines
---
# Logistics.Wms.WarehouseOrderLines Entity

A planned task (operation) in a warehouse order. Entity: Wms_Warehouse_Order_Lines (Introduced in version 20.1)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseOrderLines.md#id) | guid |  
| [LineNo](Logistics.Wms.WarehouseOrderLines.md#lineno) | int32 | Unique consecutive line number within the order. [Required] 
| [Notes](Logistics.Wms.WarehouseOrderLines.md#notes) | string (nullable) | Notes for this WarehouseOrderLine. 
| [Quantity](Logistics.Wms.WarehouseOrderLines.md#quantity) | decimal | The quantity of the product, which should be operated. [Required] [Default(0)] 
| [TaskType](Logistics.Wms.WarehouseOrderLines.md#tasktype) | string | The type of the task (operation), which should be performed. MOV=Move; INB=Inbound; OUT=Outbound; INS=Inspect; PCK=Packing/Unpacking; CNT=Count. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Lot](Logistics.Wms.WarehouseOrderLines.md#lot) | [Lots](Logistics.Inventory.Lots.md) (nullable) | The lot of the product, which should be operated. null for operations, which are not lot-specific, or when any lot can be used. [Filter(multi eq)] |
| [Product](Logistics.Wms.WarehouseOrderLines.md#product) | [Products](General.Products.Products.md) | The product, which should be operated. [Required] [Filter(multi eq)] |
| [QuantityUnit](Logistics.Wms.WarehouseOrderLines.md#quantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Quantity. [Required] [Filter(multi eq)] |
| [SerialNumber](Logistics.Wms.WarehouseOrderLines.md#serialnumber) | [SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable) | The serial number of the product, which should be operated. null for operations, which are not serial number-specific, or when any serial number can be used. [Filter(multi eq)] |
| [ToUnit](Logistics.Wms.WarehouseOrderLines.md#tounit) | [MeasurementUnits](General.MeasurementUnits.md) (nullable) | Destination measurement unit. null for operations, which do not specify destination measurement unit. [Filter(multi eq)] |
| [ToWarehouseLocation](Logistics.Wms.WarehouseOrderLines.md#towarehouselocation) | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable) | Destination warehouse location. null for operations, which do not specify destination location. [Filter(multi eq)] |
| [WarehouseLocation](Logistics.Wms.WarehouseOrderLines.md#warehouselocation) | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable) | Location, where the opeartion should be performed. null for operations, which do not require location. [Filter(multi eq)] |
| [WarehouseOrder](Logistics.Wms.WarehouseOrderLines.md#warehouseorder) | [WarehouseOrders](Logistics.Wms.WarehouseOrders.md) | The [WarehouseOrder](Logistics.Wms.WarehouseOrderLines.md#warehouseorder) to which this WarehouseOrderLine belongs. [Required] [Filter(multi eq)] [Owner] |
| [WarehouseWorker](Logistics.Wms.WarehouseOrderLines.md#warehouseworker) | [WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) (nullable) | The human or robot worker, which should execute the line. null means that the line is shared among all workers, assigned to the order. [Filter(multi eq)] |
| [WarehouseZone](Logistics.Wms.WarehouseOrderLines.md#warehousezone) | [WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable) | The warehouse zone, in which the operation should be performed. null for operations which do not require specific zone. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LineNo

> Unique consecutive line number within the order. [Required]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for this WarehouseOrderLine.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> The quantity of the product, which should be operated. [Required] [Default(0)]

_Type_: **decimal**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### TaskType

> The type of the task (operation), which should be performed. MOV=Move; INB=Inbound; OUT=Outbound; INS=Inspect; PCK=Packing/Unpacking; CNT=Count. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Lot

> The lot of the product, which should be operated. null for operations, which are not lot-specific, or when any lot can be used. [Filter(multi eq)]

_Type_: **[Lots](Logistics.Inventory.Lots.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

> The product, which should be operated. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### QuantityUnit

> The measurement unit of Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### SerialNumber

> The serial number of the product, which should be operated. null for operations, which are not serial number-specific, or when any serial number can be used. [Filter(multi eq)]

_Type_: **[SerialNumbers](Logistics.Inventory.SerialNumbers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToUnit

> Destination measurement unit. null for operations, which do not specify destination measurement unit. [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### ToWarehouseLocation

> Destination warehouse location. null for operations, which do not specify destination location. [Filter(multi eq)]

_Type_: **[WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseLocation

> Location, where the opeartion should be performed. null for operations, which do not require location. [Filter(multi eq)]

_Type_: **[WarehouseLocations](Logistics.Wms.WarehouseLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrder

> The [WarehouseOrder](Logistics.Wms.WarehouseOrderLines.md#warehouseorder) to which this WarehouseOrderLine belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[WarehouseOrders](Logistics.Wms.WarehouseOrders.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseWorker

> The human or robot worker, which should execute the line. null means that the line is shared among all workers, assigned to the order. [Filter(multi eq)]

_Type_: **[WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseZone

> The warehouse zone, in which the operation should be performed. null for operations which do not require specific zone. [Filter(multi eq)]

_Type_: **[WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseOrderLines erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseOrderLines erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseOrderLines erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseOrderLines?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseOrderLines?$top=10>

