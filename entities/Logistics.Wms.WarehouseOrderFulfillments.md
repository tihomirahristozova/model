---
uid: Logistics.Wms.WarehouseOrderFulfillments
---
# Logistics.Wms.WarehouseOrderFulfillments Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

Fulfillment of a warehouse order line. Entity: Wms_Warehouse_Order_Fulfillments (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Logistics.Wms.WarehouseOrderFulfillments](Logistics.Wms.WarehouseOrderFulfillments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Logistics.Wms.WarehouseOrderFulfillments.md#creationtimeutc) | datetime | The exact time in UTC, when the fulfillment was created in the system. `Required` 
| [Id](Logistics.Wms.WarehouseOrderFulfillments.md#id) | guid |  
| [IsFinal](Logistics.Wms.WarehouseOrderFulfillments.md#isfinal) | boolean | Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities. `Required` 
| [Quantity](Logistics.Wms.WarehouseOrderFulfillments.md#quantity) | decimal (12, 3) | Fulfilled quantity in the measurement unit of the warehouse order line. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Logistics.Wms.WarehouseOrderFulfillments.md#creationuser) | [Users](Systems.Security.Users.md) | The user, who created the record. `Required` `Filter(multi eq)` |
| [WarehouseOrder](Logistics.Wms.WarehouseOrderFulfillments.md#warehouseorder) | [WarehouseOrders](Logistics.Wms.WarehouseOrders.md) | The warehouse order, which is fulfilled. `Required` `Filter(multi eq)` |
| [WarehouseOrderLine](Logistics.Wms.WarehouseOrderFulfillments.md#warehouseorderline) | [WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md) | The line for which we record fulfillment. `Required` `Filter(multi eq)` |


## Attribute Details

### CreationTimeUtc

The exact time in UTC, when the fulfillment was created in the system. `Required`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsFinal

Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities. `Required`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

Fulfilled quantity in the measurement unit of the warehouse order line. `Required`

_Type_: **decimal (12, 3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### CreationUser

The user, who created the record. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrder

The warehouse order, which is fulfilled. `Required` `Filter(multi eq)`

_Type_: **[WarehouseOrders](Logistics.Wms.WarehouseOrders.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseOrderLine

The line for which we record fulfillment. `Required` `Filter(multi eq)`

_Type_: **[WarehouseOrderLines](Logistics.Wms.WarehouseOrderLines.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseOrderFulfillments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseOrderFulfillments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseOrderFulfillments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseOrderFulfillments?$top=10>

