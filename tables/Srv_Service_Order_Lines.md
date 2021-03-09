# Table Srv_Service_Order_Lines

Contains the details and problem symptoms for each object, which requires servicing. Entity: Srv_Service_Order_Lines

## Owner Tables Hierarchy

* [Srv_Service_Orders](Srv_Service_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Order_Line_Id](#service_order_line_id)|`uniqueidentifier` `PK`||
|[Service_Order_Id](#service_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number, unique within the document. Usually is increasing in steps of 10, like in 10, 20, 30, etc.|
|[Service_Object_Id](#service_object_id)|`uniqueidentifier` |The service object, which is experiencing the symptoms and needs repair.|
|[Symptom_Description](#symptom_description)|`nvarchar(254)` |Description or synopsis of the symptoms of the failed object.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Service_Object_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Symptom_Description

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


