# Table Wms_Warehouse_Locations

One physical location within a warehouse. Locations are the leaf elements of the rack structure of the warehouse. Entity: Wms_Warehouse_Locations (Introduced in version 20.1)

# Aggregate Hierarchy

* [Wms_Warehouses](Wms_Warehouses.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Location_Id|`Guid`|`PK`, Readonly||
|Location_Address|`String`||The address of the location. Should be unique within the warehouse. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this WarehouseLocation. |
