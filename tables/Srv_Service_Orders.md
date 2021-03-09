# Table Srv_Service_Orders

Service Orders are issued when a new servicing is required. Entity: Srv_Service_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Service_Order_Id](#service_order_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Customer_Id](#customer_id)|`uniqueidentifier` |The client, requesting servicing.|
|[Service_Agreement_Id](#service_agreement_id)|`uniqueidentifier` |When not NULL denotes that the order will be bound to the terms in the specified agreement.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Store_Id](#store_id)|`uniqueidentifier` |The store in which to physically store service objects, received for servicing. Need to be specified only when serviced objects are managed through warehouse; otherwise, it is null.|
|[Ship_To_Customer_Id](#ship_to_customer_id)|`uniqueidentifier` |Customer location of the main customer from which the service object is taken.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Service_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Service_Agreement_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Single_Execution

| Property | Value |
| - | - |
|Type|bit|

### Is_Released

| Property | Value |
| - | - |
|Type|bit|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Ship_To_Customer_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


