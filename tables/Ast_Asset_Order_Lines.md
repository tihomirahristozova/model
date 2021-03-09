# Table Ast_Asset_Order_Lines

Asset purchase or sales order line for one asset. Entity: Ast_Asset_Order_Lines

## Owner Tables Hierarchy

* [Ast_Asset_Orders](Ast_Asset_Orders.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Order_Line_Id](#asset_order_line_id)|`uniqueidentifier` `PK`||
|[Asset_Order_Id](#asset_order_id)|`uniqueidentifier` ||
|[Asset_Id](#asset_id)|`uniqueidentifier` |The asset that is acquired or retired|
|[Asset_Value](#asset_value)|`decimal(14, 2)` |Value of the acquired or retired asset|
|[Asset_Value_Currency_Id](#asset_value_currency_id)|`uniqueidentifier` |Currency of Asset Value.|
|[Quantity](#quantity)|`int` |Indicates the nature of the current operation: 1 - the operation is applied, 0 - no change, -1 - the operation is cancelled|
|[Row_Version](#row_version)|`timestamp` ||
|[Parent_Line_No](#parent_line_no)|`int` |The number of the line within the parent document, which the current line executes. NULL when the current line does not execute line.|
|[Parent_Document_Id](#parent_document_id)|`uniqueidentifier` |The document, which the current line executes. NULL when the current line does not execute another line.|

## Columns

### Asset_Order_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Value

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Asset_Value_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|int|

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


