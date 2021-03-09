# Table Exc_Tax_Warehouses

Contains excise-related data for warehouses (stores), which are defined as tax warehouses. Products subject to excise duties must be produced in tax warehouses. They can also be stored, under duty suspension, in these tax warehouses. Entity: Exc_Tax_Warehouses (Introduced in version 21.1.1.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Tax_Warehouse_Id](#tax_warehouse_id)|`uniqueidentifier` `PK`||
|[Store_Id](#store_id)|`uniqueidentifier` |The base warehouse (store), which is declared as tax warehouse.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Tax_Warehouse_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


