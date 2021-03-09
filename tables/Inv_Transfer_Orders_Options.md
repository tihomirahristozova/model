# Table Inv_Transfer_Orders_Options

Options per document type for the transfer orders. Entity: Inv_Transfer_Orders_Options

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transfer_Order_Option_Id](#transfer_order_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type, for which these options apply.|
|[Available_Quantity_Only](#available_quantity_only)|`bit` |Specifies, that transfer orders of this document type will be allowed to be released only when the requested quantity is less than the available (ATP) quantity.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transfer_Order_Option_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Available_Quantity_Only

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


