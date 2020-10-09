---
uid: Logistics.Wms.WarehouseLocations
---
# Logistics.Wms.WarehouseLocations Entity

One physical location within a warehouse. Locations are the leaf elements of the rack structure of the warehouse. Entity: Wms_Warehouse_Locations (Introduced in version 20.1)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Logistics.Wms.WarehouseLocations.md#id) | guid |  
| [LocationAddress](Logistics.Wms.WarehouseLocations.md#locationaddress) | string | The address of the location. Should be unique within the warehouse. [Required] [Filter(eq;like)] 
| [Notes](Logistics.Wms.WarehouseLocations.md#notes) | string (nullable) | Notes for this WarehouseLocation. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Warehouse](Logistics.Wms.WarehouseLocations.md#warehouse) | [Warehouses](Logistics.Wms.Warehouses.md) | The warehouse containing the location. [Required] [Filter(multi eq)] [Owner] |
| [WarehouseZone](Logistics.Wms.WarehouseLocations.md#warehousezone) | [WarehouseZones](Logistics.Wms.WarehouseZones.md) | The zone, which contains the location. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LocationAddress

> The address of the location. Should be unique within the warehouse. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this WarehouseLocation.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Warehouse

> The warehouse containing the location. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Warehouses](Logistics.Wms.Warehouses.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### WarehouseZone

> The zone, which contains the location. [Required] [Filter(multi eq)]

_Type_: **[WarehouseZones](Logistics.Wms.WarehouseZones.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Logistics.Wms.WarehouseLocations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Logistics.Wms.WarehouseLocations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Logistics.Wms.WarehouseLocations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_Wms_WarehouseLocations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_Wms_WarehouseLocations?$top=10>

