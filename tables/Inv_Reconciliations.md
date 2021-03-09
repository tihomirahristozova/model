# Table Inv_Reconciliations

Store reconciliations (physical counting). Usefull for real-world reconciliations and for opening balance. Entity: Inv_Reconciliations

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Reconciliation_Id](#reconciliation_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Default_Store_Id](#default_store_id)|`uniqueidentifier` |Default (but not mandatory) store for the lines. NULL means that the store should be choosed for each line.|
|[Default_Store_Bin_Id](#default_store_bin_id)|`uniqueidentifier` |The default store bin for the lines. When null, lines can specify different bins.|
|[Default_Product_Group_Id](#default_product_group_id)|`uniqueidentifier` |When not null is used to filter the product chooser for the lines.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Default_Valuation_Group_Id](#default_valuation_group_id)|`uniqueidentifier` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Reconciliation_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Product_Group_Id

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

### Default_Valuation_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


