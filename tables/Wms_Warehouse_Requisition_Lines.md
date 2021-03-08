# Table Wms_Warehouse_Requisition_Lines

Request for one product with a warehouse requisition. Entity: Wms_Warehouse_Requisition_Lines (Introduced in version 20.1)

# Aggregate Hierarchy

* [Wms_Warehouse_Requisitions](Wms_Warehouse_Requisitions.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Warehouse_Requisition_Line_Id|`Guid`|`PK`, Readonly||
|Line_No|`Int32`||The unique, consecutive line number within the requisition. `Required` |
|Notes|`String`||Notes for this WarehouseRequisitionLine. |
|Parent_Line_No|`Int32?`||The number of the line within the parent document, which the current line executes. null when the current line does not execute line. |
|Quantity_Base|`Decimal`||Quantity in the base measurement unit of the product. `Required` `Filter(multi eq;ge;le)` `Introduced in version 21.1.1.33` |
