---
uid: Logistics.Wms.WarehouseLocations
---
# Logistics.Wms.WarehouseLocations Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

One physical location within a warehouse. Locations are the leaf elements of the rack structure of the warehouse. Entity: Wms_Warehouse_Locations (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Warehouse.Name:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  
Aggregate Root:  
[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseLocations.md#id) | guid |  
| [LocationAddress](Logistics.Wms.WarehouseLocations.md#locationaddress) | string (32) | The address of the location. Should be unique within the warehouse. `Required` `Filter(eq;like)` 
| [Notes](Logistics.Wms.WarehouseLocations.md#notes) | string (max) __nullable__ | Notes for this WarehouseLocation. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Warehouse](Logistics.Wms.WarehouseLocations.md#warehouse) | [Warehouses](Logistics.Wms.Warehouses.md) | The warehouse containing the location. `Required` `Filter(multi eq)` `Owner` |
| [WarehouseZone](Logistics.Wms.WarehouseLocations.md#warehousezone) | [WarehouseZones](Logistics.Wms.WarehouseZones.md) | The zone, which contains the location. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LocationAddress

The address of the location. Should be unique within the warehouse. `Required` `Filter(eq;like)`

_Type_: **string (32)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

### Notes

Notes for this WarehouseLocation.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Warehouse

The warehouse containing the location. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### WarehouseZone

The zone, which contains the location. `Required` `Filter(multi eq)`

_Type_: **[WarehouseZones](Logistics.Wms.WarehouseZones.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseLocations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.Wms.WarehouseLocations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseLocations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseLocations?$top=10>

