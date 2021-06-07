---
uid: Logistics.Wms.WarehouseZones
---
# Logistics.Wms.WarehouseZones Entity

**Namespace:** [Logistics.Wms](Logistics.Wms.md)  

One zone within a warehouse. Each zone can have different rack structure and different temperature and other properties. Entity: Wms_Warehouse_Zones (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  
Aggregate Root:  
[Logistics.Wms.Warehouses](Logistics.Wms.Warehouses.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.Wms.WarehouseZones.md#code) | string (32) | Zone code, unique within the warehouse. `Required` `Filter(multi eq)` 
| [Id](Logistics.Wms.WarehouseZones.md#id) | guid |  
| [Name](Logistics.Wms.WarehouseZones.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multi-language name of the zone. `Required` `Filter(eq;like)` 
| [Notes](Logistics.Wms.WarehouseZones.md#notes) | string (max) __nullable__ | Notes for this WarehouseZone. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Logistics.Wms.WarehouseZones.md#parent) | [WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable) | The parent Warehouse Zone of the current Warehouse Zone. `Filter(multi eq)` |
| [Warehouse](Logistics.Wms.WarehouseZones.md#warehouse) | [Warehouses](Logistics.Wms.Warehouses.md) | The warehouse in which the zone is located. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Code

Zone code, unique within the warehouse. `Required` `Filter(multi eq)`

_Type_: **string (32)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

_Back-End Default Expression:_  
`obj.GetNextCode( obj.Parent)`

_Front-End Recalc Expressions:_  
`obj.GetNextCode( obj.Parent)`
### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multi-language name of the zone. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this WarehouseZone.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Parent

The parent Warehouse Zone of the current Warehouse Zone. `Filter(multi eq)`

_Type_: **[WarehouseZones](Logistics.Wms.WarehouseZones.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Warehouse

The warehouse in which the zone is located. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseZones erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseZones erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseZones?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseZones?$top=10>

