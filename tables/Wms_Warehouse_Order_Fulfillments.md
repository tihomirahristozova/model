# Table Wms_Warehouse_Order_Fulfillments

Fulfillment of a warehouse order line. Entity: Wms_Warehouse_Order_Fulfillments (Introduced in version 20.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Order_Fulfillment_Id](#warehouse_order_fulfillment_id)|`uniqueidentifier` `PK`||
|[Warehouse_Order_Id](#warehouse_order_id)|`uniqueidentifier` |The warehouse order, which is fulfilled.|
|[Warehouse_Order_Line_Id](#warehouse_order_line_id)|`uniqueidentifier` |The line for which we record fulfillment.|
|[Quantity](#quantity)|`decimal(12, 3)` |Fulfilled quantity in the measurement unit of the warehouse order line.|
|[Is_Final](#is_final)|`bit` |Specifies whether this fulfillment will finalize the fulfillment of the order line, regardless of any remaining quantities.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` |The user, who created the record.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The exact time in UTC, when the fulfillment was created in the system.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Order_Fulfillment_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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


