# Table Wms_Warehouse_Order_Lines

A planned task (operation) in a warehouse order. Entity: Wms_Warehouse_Order_Lines (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Wms_Warehouse_Orders](Wms_Warehouse_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Order_Line_Id](#warehouse_order_line_id)|`uniqueidentifier` `PK`||
|[Warehouse_Order_Id](#warehouse_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Unique consecutive line number within the order.|
|[Warehouse_Worker_Id](#warehouse_worker_id)|`uniqueidentifier` |Human or robot worker, which should execute the operation. NULL means that the line is shared among all workers, assigned to the order.|
|[Task_Type](#task_type)|`nvarchar(3)` Allowed: `REC`, `DES`, `MOV`, `LBL`, `INS`, `PCK`, `UPK`, `KIT`, `RKT`, `CNT`, `TSK`|The type of the task (operation), which should be performed. REC=Receive; DES=Despatch; MOV=Move; LBL=Label; INS=Inspect; PCK=Pack; UPK=Unpack; KIT=Assemble kit; RKT=Reverse kitting; CNT=Count; TSK=Task.|
|[Warehouse_Zone_Id](#warehouse_zone_id)|`uniqueidentifier` |The warehouse zone, in which the operation should be performed. NULL for operations which do not require specific zone.|
|[Warehouse_Location_Id](#warehouse_location_id)|`uniqueidentifier` |Location, where the opeartion should be performed. NULL for operations, which do not require location.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which should be used for the operation.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |The product variant, which should be used.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot of the product, which should be used. NULL for operations, which are not lot-specific, or when any lot can be used.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number of the product, which should be used. NULL for operations, which are not serial number-specific, or when any serial number can be used.|
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |Logistic unit, which should be used in the operation.|
|[Quantity](#quantity)|`decimal(12, 3)` |The quantity of the product, which should be processed.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. NULL for operations, which are not quantity-related.|
|[To_Warehouse_Location_Id](#to_warehouse_location_id)|`uniqueidentifier` |Destination warehouse location. NULL for operations, which do not specify destination location.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Warehouse_Worker_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Task_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Warehouse_Zone_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Warehouse_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


