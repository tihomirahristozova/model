# Table Exc_Tax_Warehouses


## Entity

Entity: [Finance.Excise.TaxWarehouses](~/entities/Finance.Excise.TaxWarehouses.md)

Contains excise-related data for warehouses (stores), which are defined as tax warehouses. Products subject to excise duties must be produced in tax warehouses. They can also be stored, under duty suspension, in these tax warehouses. Entity: Exc_Tax_Warehouses (Introduced in version 21.1.1.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Row_Version](#row_version)|`timestamp` ||
|[Store_Id](#store_id)|`uniqueidentifier` |The base warehouse (store), which is declared as tax warehouse.|
|[Tax_Warehouse_Excise_Number](#tax_warehouse_excise_number)|`nvarchar(32)` |The excise identification number of the tax warehouse, issued by the competent authorities.|
|[Tax_Warehouse_Id](#tax_warehouse_id)|`uniqueidentifier` `PK`||
|[Trader_Excise_Number](#trader_excise_number)|`nvarchar(32)` |The excise identification number of the owner of the Tax Warehouse.|

## Columns

### Row_Version

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|2147483647|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|timestamp|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|no|

### Store_Id


The base warehouse (store), which is declared as tax warehouse.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|None|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|1|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|yes|
|Type|uniqueidentifier|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

#### Store_Id - Supported Filters

| Filter Type | Default | Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|`NULL`|no|no|

### Tax_Warehouse_Excise_Number


The excise identification number of the tax warehouse, issued by the competent authorities.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|-|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|32|
|Order|3|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|nvarchar(32)|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|

### Tax_Warehouse_Id

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|NewGuid|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|-1|
|Order|0|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|yes (order: 1)|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|yes|
|Type|uniqueidentifier|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|no|

#### Tax_Warehouse_Id - Supported Filters

| Filter Type | Default | Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|`NULL`|no|no|

### Trader_Excise_Number


The excise identification number of the owner of the Tax Warehouse.

| Property | Value |
| - | - |
|Auto Complete|no|
|Data Filter|no|
|Default Value|-|
|Enter Stop|yes|
|Ignore for Insert Order|no|
|Is Entity Name|no|
|Max Length|32|
|Order|2|
|Ownership Reference|no|
|Pasword|no|
|Picture|no|
|Primary Key|no|
|Readonly|no|
|RTF|no|
|Sortable|no|
|Summary Type|None|
|Supports EQUALS_IN|no|
|Type|nvarchar(32)|
|UI Memo Editor|no|
|UI Width|Medium|
|User Login|no|
|Visible|yes|


