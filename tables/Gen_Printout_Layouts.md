# Table Gen_Printout_Layouts

Contains design layouts for document printouts. Entity: Gen_Printout_Layouts

## Summary

| Name | Type | Description |
| - | - | --- |
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` `PK`||
|[Printout_Layout_Name](#printout_layout_name)|`nvarchar(64)` ||
|[Document_Entity_Name](#document_entity_name)|`nvarchar(64)` |The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc.|
|[Data_Source_Id](#data_source_id)|`uniqueidentifier` |The data source for the printout|
|[Layout](#layout)|`nvarchar(2147483647)` |The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout|
|[Layout_Format](#layout_format)|`nvarchar(32)` |Format specifier of the layout. Recognized by the application|
|[Notes](#notes)|`nvarchar(254)` ||
|[Binary_Layout](#binary_layout)|`varbinary` |The printout layout, when the format requires binary storage. Alternative to Layout|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Printout_Layout_Id


Printout_Layout_Id

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
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Printout_Layout_Id](Gen_Printout_Layouts.md#printout_layout_id)|
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

### Printout_Layout_Name


Printout_Layout_Name

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Printout_Layout_Name](Gen_Printout_Layouts.md#printout_layout_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|Like|None|no|no|

### Document_Entity_Name


Document_Entity_Name


The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc.


The entity name of the document type e.g. Crm_Sales_Orders, Inv_Store_Orders etc.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Document_Entity_Name](Gen_Printout_Layouts.md#document_entity_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Data_Source_Id


Data_Source_Id


The data source for the printout


The data source for the printout

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sys_Data_Sources](Sys_Data_Sources.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Data_Source_Id](Gen_Printout_Layouts.md#data_source_id)|
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
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Layout


Layout


The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout


The textual representation of the printout layout, when the format requires text representation. Alternative to Binary_Layout

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Layout](Gen_Printout_Layouts.md#layout)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Layout_Format


Layout_Format


Format specifier of the layout. Recognized by the application


Format specifier of the layout. Recognized by the application

| Property | Value |
| - | - |
|Type|nvarchar(32)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Layout_Format](Gen_Printout_Layouts.md#layout_format)|
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
|Max Length|32|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Notes](Gen_Printout_Layouts.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Binary_Layout


Binary_Layout


The printout layout, when the format requires binary storage. Alternative to Layout


The printout layout, when the format requires binary storage. Alternative to Layout

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Binary_Layout](Gen_Printout_Layouts.md#binary_layout)|
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
|Derived From|[Gen_Printout_Layouts](Gen_Printout_Layouts.md).[Row_Version](Gen_Printout_Layouts.md#row_version)|
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


