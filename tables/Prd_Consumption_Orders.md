# Table Prd_Consumption_Orders

Headers of material consuption orders of the work orders. Entity: Prd_Consumption_Orders

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Work_Order_Id](#work_order_id)|`uniqueidentifier` |The work order that will consume the materials|
|[Store_Id](#store_id)|`uniqueidentifier` |The store, from which the request for materials is made. The value is applied to all lines. NULL when the lines contain more than 1 different stores.|
|[Status](#status)|`nvarchar(1)` |N=New,P=Planned, F=Firm planned, R=Released(WIP), C=Completed|
|[Document_Currency_Id](#document_currency_id)|`uniqueidentifier` ||
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Order_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Status

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Document_Currency_Id

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


