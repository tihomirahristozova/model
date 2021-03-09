# Procedure Inv_Transactions_Table_Printout_Lines


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Line number, unique within the store transaction.|
|[Product_Id](#product_id)|`uniqueidentifier` |The item that was received/issued|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |The quantity of the stock received/issued in base measurement unit|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |Store bin, from/to which the transaction was performed.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` `PK`|Unique transaction line id|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Used to set the Product_Id thru the coding systems|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. NULL means that the quantity is specified only in base measurement unit|
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity received/issued in the measurement unit, specified in Quantity_Unit_Id. NULL means that the quantity is specified only in base measurement unit|
|[Line_Base_Cost](#line_base_cost)|`decimal(0, 0)` ||
|[Line_Store_Cost](#line_store_cost)|`decimal(0, 0)` ||
|[Line_Product_Cost](#line_product_cost)|`decimal(0, 0)` ||
|[Line_Document_Cost](#line_document_cost)|`decimal(14, 2)` Readonly|The cost of the transaction in the currency of the document|
|[Line_Cost](#line_cost)|`decimal(14, 2)` |Total cost for the line|
|[Unit_Cost](#unit_cost)|`decimal(14, 5)` |Cost for 1 of the specified quantity|
|[Finished](#finished)|`bit` |1 if this transaction entry completes the operation. 0 if there might be more entries|
|[Notes](#notes)|`nvarchar` ||
|[Quantity_Unit_Id_Text](#quantity_unit_id_text)|`nvarchar` `ML`||
|[Quantity_Unit_Name](#quantity_unit_name)|`nvarchar` `ML`|Name of the measurement unit|
|[Lot_Number](#lot_number)|`nvarchar` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Product_Name](#product_name)|`nvarchar` `ML`|Name of the item|
|[Part_Number](#part_number)|`nvarchar` |Unique part number of the product|
|[Original_Product_Id](#original_product_id)|`uniqueidentifier` |When specified, contains the original product, which was ordered to be received or issued. The actual product is recorded in the Product field. Deprecated. Use Parent Store Order Line.Product instead.|
|[Store_Name](#store_name)|`nvarchar` `ML`|Name of the store|
|[Parent_Store_Order_Line_Id](#parent_store_order_line_id)|`uniqueidentifier` |The line, containing the ordered quantity, which this execution line executes.|
|[Transaction_Id](#transaction_id)|`uniqueidentifier` |The transaction to which the transaction line belongs.|
|[Temp_Order_No](#temp_order_no)|`nvarchar` |Obsolete. Not used.|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` |Exact time when the transaction changes the cost of the product|

## Columns

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Product_Id

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

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Line_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Line_Document_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Unit_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Quantity_Unit_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Part_Number

| Property | Value |
| - | - |
|Type|nvarchar|

### Original_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Parent_Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Temp_Order_No

| Property | Value |
| - | - |
|Type|nvarchar|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|


