---
uid: Logistics.Wms.WarehouseOrders
---
# Logistics.Wms.WarehouseOrders

Contains order for internal warehouse operation or plan for execution of warehouse requisition. Entity: Wms_Warehouse_Orders (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseOrders.md#Id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Document](Logistics.Wms.WarehouseOrders.md#Document) | [General.Documents](General.Documents.md) | The [Document](General.Documents.md) to which this WarehouseOrder belongs. [Required] [Filter(multi eq)] [Owner] |
| [Warehouse](Logistics.Wms.WarehouseOrders.md#Warehouse) | [Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md) | The warehouse, where the order will be executed. [Required] [Filter(multi eq)] |
| [WarehouseWorker](Logistics.Wms.WarehouseOrders.md#WarehouseWorker) | [Logistics.Wms.WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) (nullable) | When set, denotes that the whole order is assigned to the specified worker. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Lines | [Logistics.Wms.WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md) | List of [WarehouseOrderLine](Logistics.Wms.WarehouseOrderLines.md) child objects, based on the [Logistics.Wms.WarehouseOrderLine.WarehouseOrder](Logistics.Wms.WarehouseOrderLines.md#WarehouseOrder) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  


## Reference Details

### Document

> The [Document](General.Documents.md) to which this WarehouseOrder belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Documents](General.Documents.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Warehouse

> The warehouse, where the order will be executed. [Required] [Filter(multi eq)]

_Type_: **[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WarehouseWorker

> When set, denotes that the whole order is assigned to the specified worker. [Filter(multi eq)]

_Type_: **[Logistics.Wms.WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseOrders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseOrders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseOrders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseOrders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseOrders?$top=10>

