# Table Wms_Warehouse_Requisition_Lines

Request for one product with a warehouse requisition. Entity: Wms_Warehouse_Requisition_Lines (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Wms_Warehouse_Requisitions](Wms_Warehouse_Requisitions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Requisition_Line_Id](#warehouse_requisition_line_id)|`uniqueidentifier` `PK`||
|[Warehouse_Requisition_Id](#warehouse_requisition_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |The unique, consecutive line number within the requisition.|
|[Product_Id](#product_id)|`uniqueidentifier` |The requested product.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The requested lot. NULL means that any lot can be used or the product does not use lots at all.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The requested serial number. NULL means that any serial number can be used or the product does not use serial numbers at all.|
|[Quantity](#quantity)|`decimal(12, 3)` |The requested quantity.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute line.|
|[Quantity_Base](#quantity_base)|`decimal(12, 3)` |Quantity in the base measurement unit of the product.|

## Columns

### Warehouse_Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

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

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Quantity_Unit_Id

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

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(12, 3)|


