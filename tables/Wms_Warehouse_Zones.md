# Table Wms_Warehouse_Zones

One zone within a warehouse. Each zone can have different rack structure and different temperature and other properties. Entity: Wms_Warehouse_Zones (Introduced in version 20.1)

# Aggregate Hierarchy

* [Wms_Warehouses](Wms_Warehouses.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Zone_Id|`Guid`|`PK`, Readonly||
|Warehouse_Zone_Code|`String`||Zone code, unique within the warehouse. `Required` `Filter(multi eq)` |
|Warehouse_Zone_Name|`MultilanguageString`||Multi-language name of the zone. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this WarehouseZone. |
