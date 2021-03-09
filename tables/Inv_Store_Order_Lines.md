# Table Inv_Store_Order_Lines

Detail lines of store orders. Each line represents one planned stock transaction line, but can be executed in parts. E.g. many transaction lines can be bound to one order line. Entity: Inv_Store_Order_Lines

## Owner Tables Hierarchy

* [Inv_Store_Orders](Inv_Store_Orders.md)
* [Gen_Documents](Gen_Documents.md)

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
|[Lot_Number](#lot_number)|`nvarchar(16)` |Obsolete. Not used.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Which serial number to receive/issue. NULL means that serial number is unknown or not applicable|
|[Sales_Order_Line_Id](#sales_order_line_id)|`uniqueidentifier` |Sales order line which is managed by this store order line. When specified sales order line is used to make the margin analysis.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Transaction_Timestamp](#transaction_timestamp)|`datetime` Readonly|Exact time when the transaction for this store order line changes the cost of the product|
|[For_Ordering](#for_ordering)|`bit` |Specifies that the quantity of the product can be less than free to use quantity, because the product will be supplied |
|[Persist_Lot](#persist_lot)|`bit` |If checked specifies that the lot in the line cannot be changed in the sub-documents created by the current document.|
|[Store_Order_Line_Id](#store_order_line_id)|`uniqueidentifier` `PK`|Store order line Id|
|[Parent_Line_Id](#parent_line_id)|`uniqueidentifier` |Id of the line of the parent document, which generated the store order. NULL for user-entered store orders or if not applicable|
|[Store_Order_Id](#store_order_id)|`uniqueidentifier` ||
|[Lot_Id](#lot_id)|`uniqueidentifier` |If non-null, contains the specific lot to use for the movement|
|[Line_Cost](#line_cost)|`decimal(14, 2)` |Total cost for the line in the currency of the document. Equals Quantity * Unit_Cost|
|[Unit_Cost](#unit_cost)|`decimal(14, 5)` |Cost for 1 unit of measure in the currency of the document|
|[Product_Variant_Id](#product_variant_id)|`uniqueidentifier` |If specified determines which product variant of the current product in this line is used.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute parent line.|
|[Row_Version](#row_version)|`timestamp` ||
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

### Lot_Number

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Serial_Number_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Sales_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Transaction_Timestamp

| Property | Value |
| - | - |
|Type|datetime|

### For_Ordering

| Property | Value |
| - | - |
|Type|bit|

### Persist_Lot

| Property | Value |
| - | - |
|Type|bit|

### Store_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lot_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Unit_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 5)|

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
|Type|decimal(18, 3)|


