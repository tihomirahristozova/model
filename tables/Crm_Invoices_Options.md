# Table Crm_Invoices_Options

Default options for user document types for Invoices. Entity: Crm_Invoices_Options

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Invoices_Option_Id](#invoices_option_id)|`uniqueidentifier` `PK`||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type for which the invoice option applies.|
|[Default_Deal_Type_Id](#default_deal_type_id)|`uniqueidentifier` |When not NULL, specifies default VAT deal type.|
|[Sign_Restriction](#sign_restriction)|`int` Allowed: `-1`, `0`, `1`|Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts|
|[Total_Amount_Sign_Restriction](#total_amount_sign_restriction)|`int` Allowed: `-1`, `0`, `1`|Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts|
|[VAT_Deviation_Document_Amount_Type_Id](#vat_deviation_document_amount_type_id)|`uniqueidentifier` |Document amount that contains the difference between the total amount of the invoice formed by unit prices with VAT and the amount formed by unit prices without VAT|
|[Creates_VAT_Entries](#creates_vat_entries)|`bit` |Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Invoices_Option_Id


Invoices_Option_Id

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
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Invoices_Option_Id](Crm_Invoices_Options.md#invoices_option_id)|
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

### Document_Type_Id


Document_Type_Id


The document type for which the invoice option applies.


The document type for which the invoice option applies.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Document_Types](Gen_Document_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Document_Type_Id](Crm_Invoices_Options.md#document_type_id)|
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

### Default_Deal_Type_Id


Default_Deal_Type_Id


When not NULL, specifies default VAT deal type.


When not NULL, specifies default VAT deal type.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[VAT_Deal_Types](VAT_Deal_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Default_Deal_Type_Id](Crm_Invoices_Options.md#default_deal_type_id)|
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
|Equals|NULL|yes|no|

### Sign_Restriction


Sign_Restriction


Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts


Restricts the sign of the line amounts of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts

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
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Sign_Restriction](Crm_Invoices_Options.md#sign_restriction)|
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


Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts


Restricts the sign of the total amount (amount to pay) of the invoices. -1 =allow only negative, 0=allow all, 1=allow only positive amounts

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
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Total_Amount_Sign_Restriction](Crm_Invoices_Options.md#total_amount_sign_restriction)|
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

### VAT_Deviation_Document_Amount_Type_Id


VAT_Deviation_Document_Amount_Type_Id


Document amount that contains the difference between the total amount of the invoice formed by unit prices with VAT and the amount formed by unit prices without VAT


Document amount that contains the difference between the total amount of the invoice formed by unit prices with VAT and the amount formed by unit prices without VAT

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Document_Amount_Types](Gen_Document_Amount_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[VAT_Deviation_Document_Amount_Type_Id](Crm_Invoices_Options.md#vat_deviation_document_amount_type_id)|
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
|Equals|NULL|yes|no|

### Creates_VAT_Entries


Creates_VAT_Entries


Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided.


Specifies whether the invoices of the current type create entries in the VAT ledges. If is used, for instance, to determine if null VAT entry should be automatically created when the invoice is voided.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Creates_VAT_Entries](Crm_Invoices_Options.md#creates_vat_entries)|
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
|Derived From|[Crm_Invoices_Options](Crm_Invoices_Options.md).[Row_Version](Crm_Invoices_Options.md#row_version)|
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


