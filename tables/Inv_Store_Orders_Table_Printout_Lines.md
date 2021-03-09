# Procedure Inv_Store_Orders_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Line number within the store order|
|[Product_Id](#product_id)|`uniqueidentifier` |The product which should be received/issued|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity ordered for receipt/issue|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` Readonly|Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |From/to which store bin to issue/receive the products. NULL means that the store bin is unknown or not applicable|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[L4_Name](#l4_name)|`nvarchar` ||
|[L3_Name](#l3_name)|`nvarchar` ||
|[L2_Name](#l2_name)|`nvarchar` ||
|[L1_Name](#l1_name)|`nvarchar` ||
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` Readonly|Exact time when the transaction for this store order line changes the cost of the product|
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` |Sales order line which is managed by this store order line. When specified sales order line is used to make the margin analysis.|
|[Line_Cost](#line_cost)|`decimal(0, 0)` ||
|[Unit_Cost](#unit_cost)|`decimal(0, 0)` ||
|[Lot_Number](#lot_number)|`nvarchar` |Obsolete. Not used.|
|[Store_Order_Line_Id](#store_order_line_id)|`uniqueidentifier` `PK`|Store order line Id|
|[Current_Quantity](#current_quantity)|`decimal(0, 0)` ||
|[L5_Name](#l5_name)|`nvarchar` ||
|[Quantity_Unit_Name](#quantity_unit_name)|`nvarchar` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Store_Bin_Name](#store_bin_name)|`nvarchar` ||
|[Part_Number](#part_number)|`nvarchar` ||
|[Product_Name](#product_name)|`nvarchar` ||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Store_Order_Id](#store_order_id)|`uniqueidentifier` ||
|[Quantity_Base_Unit_Name](#quantity_base_unit_name)|`nvarchar` ||
|[L6_Name](#l6_name)|`nvarchar` ||

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Guarantee_Period_Days

| Property | Value |
| - | - |
|Type|int|

### L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Current_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Unit_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Bin_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Part_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base_Unit_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


