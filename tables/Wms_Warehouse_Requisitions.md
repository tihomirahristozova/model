# Table Wms_Warehouse_Requisitions

Contains request for warehouse operation created from another module. Entity: Wms_Warehouse_Requisitions (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Requisition_Id](#warehouse_requisition_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse, for which the operation is requested.|
|[Requisition_Type](#requisition_type)|`nvarchar(1)` Allowed: `I`, `O`|The type of the requisition. I=Inbound; O=Outbound.|
|[Row_Version](#row_version)|`timestamp` ||
|[Expected_Date](#expected_date)|`date` |Date, when the requisition is expected to be fulfilled.|
|[Expected_Time](#expected_time)|`time` |Time, when the requisition is expected to be executed. NULL when the time is unknown.|

## Columns

### Warehouse_Requisition_Id

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

### Requisition_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Expected_Date

| Property | Value |
| - | - |
|Type|date|

### Expected_Time

| Property | Value |
| - | - |
|Type|time|


