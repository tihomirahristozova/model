# Table Wms_Warehouse_Workers

Human or robot worker, which can execute warehouse tasks. Entity: Wms_Warehouse_Workers (Introduced in version 20.1)

# Aggregate Hierarchy

* [Wms_Warehouses](Wms_Warehouses.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Worker_Id|`Guid`|`PK`, Readonly||
|Active_From|`DateTime`||The date, from which the worker record has become active in the warehouse. `Required` `Default(Today)` `Filter(eq;ge;le)` |
|Active_To|`DateTime?`||The date of termination of the activity of the worker in the warehouse. Can be null for workers, which are still active and do not have previous terminations. `Filter(eq;ge;le)` |
|Is_Active|`Boolean`||Specifies whether the worker is active and can execute new warehouse tasks. `Required` `Default(true)` `Filter(eq)` |
|Warehouse_Worker_Name|`MultilanguageString`||Name of the worker (multi-language). `Required` `Filter(multi eq;like)` |
|Notes|`String`||Notes for this WarehouseWorker. |
