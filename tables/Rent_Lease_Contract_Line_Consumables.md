# Table Rent_Lease_Contract_Line_Consumables

Contains the consumables, which are sold accompanying asset rentals. Entity: Rent_Lease_Contract_Line_Consumables

## Owner Tables Hierarchy

* [Rent_Lease_Contract_Lines](Rent_Lease_Contract_Lines.md)
* [Rent_Lease_Contracts](Rent_Lease_Contracts.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Lease_Line_Consumable_Id](#lease_line_consumable_id)|`uniqueidentifier` `PK`||
|[Lease_Line_Id](#lease_line_id)|`uniqueidentifier` |Lease line with which the current consumable is given.|
|[Product_Id](#product_id)|`uniqueidentifier` |The consumable to be sold accompanying the asset.|
|[Consumable_Quantity](#consumable_quantity)|`decimal(12, 3)` |The quantity sold of the consumable.|
|[Consumable_Quantity_Unit_Id](#consumable_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Consumable Quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |Store from which the consumable is issued.|
|[Line_No](#line_no)|`int` |Consecutive number of the consumable within the lease contract line.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Lease_Line_Consumable_Id


Lease_Line_Consumable_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Lease_Line_Consumable_Id](Rent_Lease_Contract_Line_Consumables.md#lease_line_consumable_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Lease_Line_Id


Lease_Line_Id


Lease line with which the current consumable is given.


Lease line with which the current consumable is given.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Rent_Lease_Contract_Lines](Rent_Lease_Contract_Lines.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Lease_Line_Id](Rent_Lease_Contract_Line_Consumables.md#lease_line_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Product_Id


Product_Id


The consumable to be sold accompanying the asset.


The consumable to be sold accompanying the asset.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Products](Gen_Products.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Product_Id](Rent_Lease_Contract_Line_Consumables.md#product_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Consumable_Quantity


Consumable_Quantity


The quantity sold of the consumable.


The quantity sold of the consumable.

| Property | Value |
| - | - |
|Type|decimal(12, 3)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Consumable_Quantity](Rent_Lease_Contract_Line_Consumables.md#consumable_quantity)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Consumable_Quantity_Unit_Id


Consumable_Quantity_Unit_Id


The measurement unit of Consumable Quantity.


The measurement unit of Consumable Quantity.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Measurement_Units](Gen_Measurement_Units.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Consumable_Quantity_Unit_Id](Rent_Lease_Contract_Line_Consumables.md#consumable_quantity_unit_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Store_Id


Store_Id


Store from which the consumable is issued.


Store from which the consumable is issued.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Inv_Stores](Inv_Stores.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Store_Id](Rent_Lease_Contract_Line_Consumables.md#store_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Line_No


Line_No


Consecutive number of the consumable within the lease contract line.


Consecutive number of the consumable within the lease contract line.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Autoincrement|10|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Line_No](Rent_Lease_Contract_Line_Consumables.md#line_no)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|no|yes|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Rent_Lease_Contract_Line_Consumables](Rent_Lease_Contract_Line_Consumables.md).[Row_Version](Rent_Lease_Contract_Line_Consumables.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


