# Table Scm_Purchase_Invoices_Options

Contains purchase invoice specific options for the different document types. Entity: Scm_Purchase_Invoices_Options

## Summary

| Name | Type | Description |
| - | - | --- |
|[Purchese_Invoices_Option_Id](#purchese_invoices_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type, for which the options are specified.|
|[Sign_Restriction](#sign_restriction)|`int` Allowed: `-1`, `0`, `1`|This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type.|
|[Total_Amount_Sign_Restriction](#total_amount_sign_restriction)|`int` Allowed: `-1`, `0`, `1`|This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Purchese_Invoices_Option_Id


Purchese_Invoices_Option_Id

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
|Derived From|[Scm_Purchase_Invoices_Options](Scm_Purchase_Invoices_Options.md).[Purchese_Invoices_Option_Id](Scm_Purchase_Invoices_Options.md#purchese_invoices_option_id)|
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

### Document_Type_Id


Document_Type_Id


The document type, for which the options are specified.


The document type, for which the options are specified.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Scm_Purchase_Invoices_Options](Scm_Purchase_Invoices_Options.md).[Document_Type_Id](Scm_Purchase_Invoices_Options.md#document_type_id)|
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

### Sign_Restriction


Sign_Restriction


This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type.


This option can restrict the sign of the Line Amounts for each detail line in purchase invoices of the specified document type.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`-1`, `0`, `1`|
|Default Value|0|
|Derived From|[Scm_Purchase_Invoices_Options](Scm_Purchase_Invoices_Options.md).[Sign_Restriction](Scm_Purchase_Invoices_Options.md#sign_restriction)|
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

### Total_Amount_Sign_Restriction


Total_Amount_Sign_Restriction


This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release.


This option can restrict the sign of the Total Amounts of the purchase invoices of the specified document type. The restriction is applied upon document Release.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`-1`, `0`, `1`|
|Default Value|0|
|Derived From|[Scm_Purchase_Invoices_Options](Scm_Purchase_Invoices_Options.md).[Total_Amount_Sign_Restriction](Scm_Purchase_Invoices_Options.md#total_amount_sign_restriction)|
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
|Derived From|[Scm_Purchase_Invoices_Options](Scm_Purchase_Invoices_Options.md).[Row_Version](Scm_Purchase_Invoices_Options.md#row_version)|
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


