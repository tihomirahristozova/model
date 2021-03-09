# Table Inv_Transfer_Orders

Orders for stock transfers between stores. Entity: Inv_Transfer_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transfer_Order_Id](#transfer_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The unique stock transfer order id, as per documents table|
|[Default_Due_Date_Out](#default_due_date_out)|`datetime` |When the transfer is scheduled to issue the goods from the source warehouse|
|[Default_Due_Date_In](#default_due_date_in)|`datetime` |The date, when the goods are expected to be received in the destination warehouse|
|[From_Store_Id](#from_store_id)|`uniqueidentifier` |Specifies the store, from which the goods will be issued.|
|[To_Store_Id](#to_store_id)|`uniqueidentifier` |Specifies the store, in which the goods will be received.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Status](#status)|`smallint` Allowed: `1`, `2`|Obsolete. Not used. (Status of the transfer document: 1-Open for editing; 2-Released)|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transfer_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Due_Date_Out

| Property | Value |
| - | - |
|Type|datetime|

### Default_Due_Date_In

| Property | Value |
| - | - |
|Type|datetime|

### From_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Status

| Property | Value |
| - | - |
|Type|smallint|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


