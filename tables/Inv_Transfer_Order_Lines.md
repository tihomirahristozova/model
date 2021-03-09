# Table Inv_Transfer_Order_Lines

Details of Transfer Orders. Each line contains order for the movement of one product. Entity: Inv_Transfer_Order_Lines

## Owner Tables Hierarchy

* [Inv_Transfer_Orders](Inv_Transfer_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Ord](#line_ord)|`int` |Line ordinal position within the transaction. Duplicates are allowed, but not advised|
|[Product_Id](#product_id)|`uniqueidentifier` |The product which will be transferred|
|[From_Store_Bin_Id](#from_store_bin_id)|`uniqueidentifier` |From which store bin to issue/receive the products. NULL means that the store bin is unknown or not applicable|
|[To_Store_Bin_Id](#to_store_bin_id)|`uniqueidentifier` |To which store bin to issue/receive the products. NULL means that the store bin is unknown or not applicable|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Quantity](#quantity)|`decimal(18, 3)` |Quantity ordered for transfer|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |Quantity in the base (default) measurement unit of the Item (calculated at the time of last update of the current store order line). Should be updated in parallel with each Quantity update|
|[Due_Date_Out](#due_date_out)|`datetime` |When this line of the transfer is scheduled to issue the goods from the source warehouse. Initially copied from the transfer header|
|[Due_Date_In](#due_date_in)|`datetime` |The date, when the goods are expected to be received in the destination warehouse. Initially copied from the transfer header|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Selects the product thru some of the product codes.|
|[Standard_Unit_Price](#standard_unit_price)|`decimal(14, 5)` |Standard unit price of the product during the creation of the transfer order line|
|[Notes](#notes)|`nvarchar(254)` ||
|[Transfer_Order_Id](#transfer_order_id)|`uniqueidentifier` |The parent transfer order|
|[Transfer_Order_Line_Id](#transfer_order_line_id)|`uniqueidentifier` `PK`||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Row_Version](#row_version)|`timestamp` ||
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

## Columns

### Line_Ord

| Property | Value |
| - | - |
|Type|int|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Store_Bin_Id

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
|Type|decimal(18, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

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

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Unit_Price

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Transfer_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transfer_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


