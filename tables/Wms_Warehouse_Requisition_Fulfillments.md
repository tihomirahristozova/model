# Table Wms_Warehouse_Requisition_Fulfillments

Fulfillment ledger for warehouse requisitions. Entity: Wms_Warehouse_Requisition_Fulfillments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Requisition_Fulfillment_Id](#warehouse_requisition_fulfillment_id)|`uniqueidentifier` `PK`||
|[Warehouse_Requisition_Id](#warehouse_requisition_id)|`uniqueidentifier` |The warehouse requisiton, which is fulfilled.|
|[Warehouse_Requisition_Line_Id](#warehouse_requisition_line_id)|`uniqueidentifier` |The requisition line, which is fulfilled.|
|[Fulfillment_Type](#fulfillment_type)|`nvarchar(1)` |Type of fulfillment: P=Plan created; C=Requisition completed.|
|[Quantity](#quantity)|`decimal(12, 3)` |Quantity fulfilled (in the measurement unit of the requisition line).|
|[Is_Final](#is_final)|`bit` |Specifies whether this fulfillment finalizes the requisition line, regardless of any remaining quantities.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the record.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact time in UTC, when the fulfillment was created in the system.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Requisition_Fulfillment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Requisition_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Requisition_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Fulfillment_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Is_Final

| Property | Value |
| - | - |
|Type|bit|

### Creation_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


