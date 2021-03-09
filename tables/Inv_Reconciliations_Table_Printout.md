# Procedure Inv_Reconciliations_Table_Printout


## Summary

| Name | Type | Description |
| - | - | --- |
|[Reconciliation_Id](#reconciliation_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[Default_Store_Id](#default_store_id)|`uniqueidentifier` |Default (but not mandatory) store for the lines. NULL means that the store should be choosed for each line.|
|[Default_Store_Id_Text](#default_store_id_text)|`nvarchar` `ML`||
|[Store_Responsible_Party_Name](#store_responsible_party_name)|`nvarchar` ||
|[Default_Store_Bin_Id](#default_store_bin_id)|`uniqueidentifier` |The default store bin for the lines. When null, lines can specify different bins.|
|[Default_Product_Group_Id](#default_product_group_id)|`uniqueidentifier` |When not null is used to filter the product chooser for the lines.|

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

### Default_Store_Id_Text

| Property | Value |
| - | - |
|Type|nvarchar|

### Store_Responsible_Party_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Default_Store_Bin_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Product_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


