# Table Wms_Warehouses

Physical warehouse. Entity: Wms_Warehouses (Introduced in version 20.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Id|`Guid`|`PK`, Readonly||
|Warehouse_Name|`MultilanguageString`||Name of the warehouse (multilanguage). `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this Warehouse. |
