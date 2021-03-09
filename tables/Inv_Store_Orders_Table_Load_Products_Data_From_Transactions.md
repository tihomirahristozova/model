# Procedure Inv_Store_Orders_Table_Load_Products_Data_From_Transactions


## Summary

| Name | Type | Description |
| - | - | --- |
|[Store_Order_Line_Id](#store_order_line_id)|`uniqueidentifier` ||
|[Store_Order_Id](#store_order_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` ||
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` ||
|[Quantity](#quantity)|`decimal(0, 0)` ||
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` ||
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` ||
|[Lot_Number](#lot_number)|`nvarchar` ||
|[Unit_Cost](#unit_cost)|`decimal(0, 0)` ||
|[Line_Cost](#line_cost)|`decimal(0, 0)` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` ||
|[Guarantee_Period_Days](#guarantee_period_days)|`int` ||
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` ||
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` ||
|[For_Ordering](#for_ordering)|`bit` ||
|[Notes](#notes)|`nvarchar` ||
|[Persist_Lot](#persist_lot)|`bit` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` ||
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` ||
|[Parent_Line_No](#parent_line_no)|`int` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(0, 0)` ||
|[Actual_Transaction_Line_Id](#actual_transaction_line_id)|`uniqueidentifier` ||
|[Actual_Transaction_Timestamp](#actual_transaction_timestamp)|`datetime` ||
|[Actual_Lot_Id](#actual_lot_id)|`uniqueidentifier` ||
|[Actual_Serial_Number_Id](#actual_serial_number_id)|`uniqueidentifier` ||
|[Actual_Quantity_Base](#actual_quantity_base)|`decimal(0, 0)` ||
|[Actual_Quantity](#actual_quantity)|`decimal(0, 0)` ||
|[Actual_Quantity_Unit_Id](#actual_quantity_unit_id)|`uniqueidentifier` ||
|[Actual_Line_Document_Cost](#actual_line_document_cost)|`decimal(0, 0)` ||
|[Actual_Cost_Currency_Id](#actual_cost_currency_id)|`uniqueidentifier` ||
|[Actual_Line_Store_Cost](#actual_line_store_cost)|`decimal(0, 0)` ||
|[Actual_Store_Cost_Currency_Id](#actual_store_cost_currency_id)|`uniqueidentifier` ||
|[Actual_Line_Product_Cost](#actual_line_product_cost)|`decimal(0, 0)` ||
|[Actual_Product_Cost_Currency_Id](#actual_product_cost_currency_id)|`uniqueidentifier` ||
|[Actual_Line_Base_Cost](#actual_line_base_cost)|`decimal(0, 0)` ||
|[Actual_Base_Cost_Currency_Id](#actual_base_cost_currency_id)|`uniqueidentifier` ||
|[Actual_Transaction_Line_Finished](#actual_transaction_line_finished)|`bit` ||
|[Actual_Product_Variant_Id](#actual_product_variant_id)|`uniqueidentifier` ||

## Columns

### Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Id

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
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### For_Ordering

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Persist_Lot

| Property | Value |
| - | - |
|Type|bit|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Actual_Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Line_Document_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Cost_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Line_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Store_Cost_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Line_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Product_Cost_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Line_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Actual_Base_Cost_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Actual_Transaction_Line_Finished

| Property | Value |
| - | - |
|Type|bit|

### Actual_Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


