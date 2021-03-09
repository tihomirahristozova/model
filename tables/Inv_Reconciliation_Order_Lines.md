# Table Inv_Reconciliation_Order_Lines


## Owner Tables Hierarchy

* [Inv_Reconciliation_Orders](Inv_Reconciliation_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Reconciliation_Order_Line_Id](#reconciliation_order_line_id)|`uniqueidentifier` `PK`||
|[Reconciliation_Order_Id](#reconciliation_order_id)|`uniqueidentifier` |Reconciliation order header|
|[Line_No](#line_no)|`int` |Line number within the reconciliation order|
|[Store_Id](#store_id)|`uniqueidentifier` |Store, which should be checked|
|[Product_Id](#product_id)|`uniqueidentifier` |The item which quantity should be reconciled|
|[Store_Bin_Id](#store_bin_id)|`uniqueidentifier` |Specifies store bin, that should be reconciled. NULL means to reconcile all or any bin.|
|[Serial_Number_Id](#serial_number_id)|`uniqueidentifier` |Serial number of the product, which should be reconciled.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Reconciliation_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Reconciliation_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Store_Id

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


