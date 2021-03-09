# View Wms_Warehouse_Availability_Indexed_View

The availability of goods in the warehouse locations of the warehouse. Entity: Wms_Warehouse_Availability_Indexed_View (Introduced in version 21.1.1.35)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Warehouse_Id](#warehouse_id)|`uniqueidentifier` ||
|[Warehouse_Location_Id](#warehouse_location_id)|`uniqueidentifier` |The warehouse location, where the transaction occurred.|
|[Logistic_Unit_Id](#logistic_unit_id)|`uniqueidentifier` |Logistic unit, which was transacted. NULL when the transaction was not for a logistic unit.|
|[Product_Id](#product_id)|`uniqueidentifier` |The product, which was transacted.|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |The product variant, which was transacted. NULL when the transaction was not for a product variant.|
|[Lot_Id](#lot_id)|`uniqueidentifier` |The lot which was transacted. NULL when the transaction was not for a specific lot.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |The serial number which was transacted. NULL when the transaction was not for a specific serial number.|
|[Quantity_Available](#quantity_available)|`decimal(38, 3)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of quantity.|
|[Catch_Balance](#catch_balance)|`decimal(38, 3)` ||
|[Catch_Quantity_Unit_Id](#catch_quantity_unit_id)|`uniqueidentifier` |The measurement unit of the catch quantity. NULL when catch measurement is not configured for the product.|
|[Cnt](#cnt)|`bigint` ||

## Columns

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

### Quantity_Available

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Catch_Balance

| Property | Value |
| - | - |
|Type|decimal(38, 3)|

### Catch_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cnt

| Property | Value |
| - | - |
|Type|bigint|


