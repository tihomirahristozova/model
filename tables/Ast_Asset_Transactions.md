# Table Ast_Asset_Transactions

Basic asset value transactions. The transactions can increase or decrease any of the 5 asset values. Entity: Ast_Asset_Transactions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Transaction_Id](#asset_transaction_id)|`uniqueidentifier` `PK`|Unique identification of the asset transaction.|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Asset_Transaction_Date](#asset_transaction_date)|`datetime` |Date (or end date of the period) on which the transaction takes action|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Transaction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Asset_Transaction_Date

| Property | Value |
| - | - |
|Type|datetime|

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


