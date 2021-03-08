# Table Wms_Warehouse_Order_Lines

A planned task (operation) in a warehouse order. Entity: Wms_Warehouse_Order_Lines (Introduced in version 20.1)

# Aggregate Hierarchy

* [Wms_Warehouse_Orders](Wms_Warehouse_Orders.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Order_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||Unique consecutive line number within the order. `Required` `Filter(eq)` |
|Notes|`String`||Notes for this WarehouseOrderLine. |
|Task_Type|`TaskType`|Allowed: `REC`, `DES`, `MOV`, `LBL`, `INS`, `PCK`, `UPK`, `KIT`, `RKT`, `CNT`, `TSK`|The type of the task (operation), which should be performed. REC=Receive; DES=Despatch; MOV=Move; LBL=Label; INS=Inspect; PCK=Pack; UPK=Unpack; KIT=Assemble kit; RKT=Reverse kitting; CNT=Count; TSK=Task. `Required` `Filter(multi eq)` |
