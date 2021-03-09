# Procedure Inv_Transfer_Orders_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Transfer_Order_Id](#transfer_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The unique stock transfer order id, as per documents table|
|[Default_Due_Date_Out](#default_due_date_out)|`datetime` |When the transfer is scheduled to issue the goods from the source warehouse|
|[Default_Due_Date_In](#default_due_date_in)|`datetime` |The date, when the goods are expected to be received in the destination warehouse|
|[From_Store_Id](#from_store_id)|`uniqueidentifier` |Specifies the store, from which the goods will be issued.|
|[From_Store_Id_Text](#from_store_id_text)|`nvarchar` ||
|[To_Store_Id](#to_store_id)|`uniqueidentifier` |Specifies the store, in which the goods will be received.|
|[To_Store_Id_Text](#to_store_id_text)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Status](#status)|`smallint` Allowed: `1`, `2`|Obsolete. Not used. (Status of the transfer document: 1-Open for editing; 2-Released)|

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

### From_Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### To_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### To_Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Status

| Property | Value |
| - | - |
|Type|smallint|


