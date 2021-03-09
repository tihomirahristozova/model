# Procedure Inv_Transfer_Orders_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Transfer_Order_Line_Id](#transfer_order_line_id)|`uniqueidentifier` `PK`||
|[Transfer_Order_Id](#transfer_order_id)|`uniqueidentifier` |The parent transfer order|
|[Line_Ord](#line_ord)|`int` |Line ordinal position within the transaction. Duplicates are allowed, but not advised|
|[Product_Id](#product_id)|`uniqueidentifier` |The product which will be transferred|
|[Product_Id_Text](#product_id_text)|`nvarchar` ||
|[Product_Name](#product_name)|`nvarchar` ||
|[From_Store_Bin_Id](#from_store_bin_id)|`uniqueidentifier` |From which store bin to issue/receive the products. NULL means that the store bin is unknown or not applicable|
|[From_Store_Bin_Id_Text](#from_store_bin_id_text)|`nvarchar` ||
|[To_Store_Bin_Id](#to_store_bin_id)|`uniqueidentifier` |To which store bin to issue/receive the products. NULL means that the store bin is unknown or not applicable|
|[To_Store_Bin_Id_Text](#to_store_bin_id_text)|`nvarchar` ||
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Serial_Number_Id_Text](#serial_number_id_text)|`nvarchar` ||
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity ordered for transfer|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` ||
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update|
|[Due_Date_Out](#due_date_out)|`datetime` |When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header|
|[Due_Date_In](#due_date_in)|`datetime` |The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|

## Columns

### Transfer_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transfer_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### From_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Store_Bin_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### To_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Store_Bin_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Due_Date_Out

| Property | Value |
| - | - |
|Type|datetime|

### Due_Date_In

| Property | Value |
| - | - |
|Type|datetime|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


