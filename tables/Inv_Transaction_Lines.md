# Table Inv_Transaction_Lines

Details records of Transactions. Each detail contains the movement for one product. Entity: Inv_Transaction_Lines

## Owner Tables Hierarchy

* [Inv_Transactions](Inv_Transactions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_No](#line_no)|`int` |Line number, unique within the store transaction.|
|[Product_Id](#product_id)|`uniqueidentifier` |The item that was received/issued|
|[Quantity_Base](#quantity_base)|`decimal(18, 3)` |The quantity of the stock received/issued in base measurement unit|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |Store bin, from/to which the transaction was performed.|
|[Guarantee_Period_Days](#guarantee_period_days)|`int` |Guarantee period in days for the offered product. NULL for non-serviced products|
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Item serial number for serialized items. NULL for non-serialized items|
|[Line_Document_Cost](#line_document_cost)|`decimal(14, 2)` Readonly|The cost of the transaction in the currency of the document|
|[Line_Product_Cost](#line_product_cost)|`decimal(14, 2)` Readonly|The cost of the transaction in the currency of the product|
|[Line_Cost](#line_cost)|`decimal(14, 2)` |Total cost for the line|
|[Line_Store_Cost](#line_store_cost)|`decimal(14, 2)` Readonly|The cost of the transaction in the currency of the warehouse|
|[Product_Code_Id](#product_code_id)|`uniqueidentifier` |Used to set the Product_Id thru the coding systems|
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` |Exact time when the transaction changes the cost of the product|
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` |Used, when transaction lines are generated directly from other entities (different from Store Order). Denotes the Id of the parent document line, which generated the transaction line.|
|[Line_Base_Cost](#line_base_cost)|`decimal(14, 2)` |The cost of the transaction in the currency of the enterprise company|
|[Allow_Over_Execution](#allow_over_execution)|`bit` |When true, specifies, that we explicitly allow over-execution. Over-execution is when the quantity in all execution lines exceed the quantity in the parent store order line.|
|[Original_Product_Id](#original_product_id)|`uniqueidentifier` |When specified, contains the original product, which was ordered to be received or issued. The actual product is recorded in the Product field. Deprecated. Use Parent Store Order Line.Product instead.|
|[Quantity](#quantity)|`decimal(18, 3)` |The quantity received/issued in the measurement unit, specified in Quantity_Unit_Id. NULL means that the quantity is specified only in base measurement unit|
|[Parent_Store_Order_Line_Id](#parent_store_order_line_id)|`uniqueidentifier` |The line, containing the ordered quantity, which this execution line executes.|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` `PK`|Unique transaction line id|
|[Transaction_Id](#transaction_id)|`uniqueidentifier` |The transaction to which the transaction line belongs.|
|[Finished](#finished)|`bit` |1 if this transaction entry completes the operation. 0 if there might be more entries|
|[Unit_Cost](#unit_cost)|`decimal(14, 5)` |Cost for 1 of the specified quantity|
|[Temp_Order_No](#temp_order_no)|`nvarchar(50)` |Obsolete. Not used.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. NULL means that the quantity is specified only in base measurement unit|
|[Notes](#notes)|`nvarchar(254)` ||
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute line.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Standard_Quantity_Base](#standard_quantity_base)|`decimal(18, 3)` Readonly|The theoretical quantity in base measurement unit according to the current measurement dimensions for the product. Used to measure the execution.|

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

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Document_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Product_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Line_Store_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Product_Code_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Base_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Allow_Over_Execution

| Property | Value |
| - | - |
|Type|bit|

### Original_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Parent_Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Finished

| Property | Value |
| - | - |
|Type|bit|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

### Temp_Order_No

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Product_Variant_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Parent_Line_No

| Property | Value |
| - | - |
|Type|int|

### Parent_Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(18, 3)|


