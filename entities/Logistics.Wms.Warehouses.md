---
uid: Logistics.Wms.Warehouses
---
# Logistics.Wms.Warehouses

Physical warehouse. Entity: Wms_Warehouses (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.Warehouses.md#Id) | guid |  
| [Notes](Logistics.Wms.Warehouses.md#Notes) | string (nullable) | Notes for this Warehouse. 
| [Name](Logistics.Wms.Warehouses.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Name of the warehouse (multilanguage). [Required] [Filter(eq;like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Locations | [Logistics.Wms.WarehouseLocations](Logistics.Wms.WarehouseLocations.md) | List of [WarehouseLocation](Logistics.Wms.WarehouseLocations.md) child objects, based on the [Logistics.Wms.WarehouseLocation.Warehouse](Logistics.Wms.WarehouseLocations.md#Warehouse) back reference 
| Workers | [Logistics.Wms.WarehouseWorkers](Logistics.Wms.WarehouseWorkers.md) | List of [WarehouseWorker](Logistics.Wms.WarehouseWorkers.md) child objects, based on the [Logistics.Wms.WarehouseWorker.Warehouse](Logistics.Wms.WarehouseWorkers.md#Warehouse) back reference 
| Zones | [Logistics.Wms.WarehouseZones](Logistics.Wms.WarehouseZones.md) | List of [WarehouseZone](Logistics.Wms.WarehouseZones.md) child objects, based on the [Logistics.Wms.WarehouseZone.Warehouse](Logistics.Wms.WarehouseZones.md#Warehouse) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this Warehouse.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> Name of the warehouse (multilanguage). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
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

