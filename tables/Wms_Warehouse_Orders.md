# Table Wms_Warehouse_Orders

Contains order for internal warehouse operation or plan for execution of warehouse requisition. Entity: Wms_Warehouse_Orders (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Order_Id](#warehouse_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse, where the order will be executed.|
|[Row_Version](#row_version)|`timestamp` ||
|[Warehouse_Worker_Id](#warehouse_worker_id)|`uniqueidentifier` |When set, denotes that the whole order is assigned to the specified worker.|

## Columns

### Warehouse_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Warehouse_Worker_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


