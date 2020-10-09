---
uid: Logistics.Wms.Warehouses
---
# Logistics.Wms.Warehouses

Physical warehouse. Entity: Wms_Warehouses (Introduced in version 20.1)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.Warehouses.md#id) | guid |  
| [Name](Logistics.Wms.Warehouses.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the warehouse (multilanguage). [Required] [Filter(eq;like)] 
| [Notes](Logistics.Wms.Warehouses.md#notes) | string (nullable) | Notes for this Warehouse. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Locations | [WarehouseLocations](Logistics.Wms.WarehouseLocations.md) | List of [WarehouseLocation](Logistics.Wms.WarehouseLocations.md) child objects, based on the [Logistics.Wms.WarehouseLocation.Warehouse](Logistics.Wms.WarehouseLocations.md#warehouse) back reference 
| Workers | [WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) | List of [WarehouseWorker](Logistics.Wms.WarehouseWorkers.md) child objects, based on the [Logistics.Wms.WarehouseWorker.Warehouse](Logistics.Wms.WarehouseWorkers.md#warehouse) back reference 
| Zones | [WarehouseZones](Logistics.Wms.WarehouseZones.md) | List of [WarehouseZone](Logistics.Wms.WarehouseZones.md) child objects, based on the [Logistics.Wms.WarehouseZone.Warehouse](Logistics.Wms.WarehouseZones.md#warehouse) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

> Name of the warehouse (multilanguage). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this Warehouse.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Logistics.Wms.Warehouses erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.Warehouses erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.Warehouses erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_Warehouses?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_Warehouses?$top=10>

