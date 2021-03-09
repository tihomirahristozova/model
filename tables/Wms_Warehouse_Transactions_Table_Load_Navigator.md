# Query Wms_Warehouse_Transactions_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Transaction_Id](#warehouse_transaction_id)|`uniqueidentifier` `PK`||
|[Warehouse_Order_Id](#warehouse_order_id)|`uniqueidentifier` |The order which created this transaction. NULL when this transaction was not based on order.|
|[Warehouse_Order_Line_Id](#warehouse_order_line_id)|`uniqueidentifier` |The order line which created this transaction. NULL when this transaction was not based on order line.|
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` |The warehouse in which the transaction occurred.|
|[Warehouse_Location_Id](#warehouse_location_id)|`uniqueidentifier` |The warehouse location, where the transaction occurred.|
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |Logistic unit, which was transacted. NULL when the transaction was not for a logistic unit.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which was transacted.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |The product variant, which was transacted. NULL when the transaction was not for a product variant.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot which was transacted. NULL when the transaction was not for a specific lot.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number which was transacted. NULL when the transaction was not for a specific serial number.|
|[Direction](#direction)|`nvarchar` Allowed: `I`, `O`|Direction of the transaction - I=IN, O=OUT.|
|[Quantity](#quantity)|`decimal(0, 0)` |The transacted net change in quantity. Positive values indicate transactions. Negative values are used for adjustments.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of quantity.|
|[Catch_Quantity](#catch_quantity)|`decimal(0, 0)` |Catch (measured) quantity for the transaction. Positive values indicate transactions. Negative values are used for adjustments. NULL when catch measurement is not configured for the product.|
|[Catch_Quantity_Unit_Id](#catch_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the catch quantity. NULL when catch measurement is not configured for the product.|
|[Creation_User_Id](#creation_user_id)|`uniqueidentifier` ||
|[Creation_Time_Utc](#creation_time_utc)|`datetime` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Warehouse_Transaction_Id

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

### Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Warehouse_Location_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Logistic_Unit_Id

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

### Direction

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Catch_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Catch_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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


