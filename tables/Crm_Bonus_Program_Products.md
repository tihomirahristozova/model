# Table Crm_Bonus_Program_Products

Provides a way to specify additional (to the one specified in Bonus Program.Conditional Product) products, which will be used to evaluate bonus program conditions. When any of the products exists in the sales document, the conditions are satisfied and the program is applied. When the conditional products list for a bonus program is empty, it is considered that the program is valid for all products. Entity: Crm_Bonus_Program_Products

## Owner Tables Hierarchy

* [Crm_Bonus_Programs](Crm_Bonus_Programs.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Bonus_Program_Product_Id](#bonus_program_product_id)|`uniqueidentifier` `PK`||
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The product which is required to exist in the final sales document in order for the bonus program to be applied|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Bonus_Program_Product_Id


Bonus_Program_Product_Id

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
|Derived From|[Crm_Bonus_Program_Products](Crm_Bonus_Program_Products.md).[Bonus_Program_Product_Id](Crm_Bonus_Program_Products.md#bonus_program_product_id)|
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
|Equals|NULL|no|yes|

### Bonus_Program_Id


Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Crm_Bonus_Programs](Crm_Bonus_Programs.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Bonus_Program_Products](Crm_Bonus_Program_Products.md).[Bonus_Program_Id](Crm_Bonus_Program_Products.md#bonus_program_id)|
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


The product which is required to exist in the final sales document in order for the bonus program to be applied


The product which is required to exist in the final sales document in order for the bonus program to be applied

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
|Derived From|[Crm_Bonus_Program_Products](Crm_Bonus_Program_Products.md).[Product_Id](Crm_Bonus_Program_Products.md#product_id)|
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
|Derived From|[Crm_Bonus_Program_Products](Crm_Bonus_Program_Products.md).[Row_Version](Crm_Bonus_Program_Products.md#row_version)|
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


