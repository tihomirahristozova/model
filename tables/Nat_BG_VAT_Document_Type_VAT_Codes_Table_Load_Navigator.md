# Query Nat_BG_VAT_Document_Type_VAT_Codes_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Type_VAT_Code_Id](#document_type_vat_code_id)|`uniqueidentifier` `PK`|Unique identification of the record.|
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |Document type that generates VAT entries.|
|[VAT_Code](#vat_code)|`nvarchar` Allowed: `01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values.|
|[Cash_Reporting_VAT_Code](#cash_reporting_vat_code)|`nvarchar` Allowed: `01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code.|

## Columns

### Document_Type_VAT_Code_Id


Document_Type_VAT_Code_Id


Unique identification of the record.


Unique identification of the record.

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
|Derived From|[Nat_BG_VAT_Document_Type_VAT_Codes](Nat_BG_VAT_Document_Type_VAT_Codes.md).[Document_Type_VAT_Code_Id](Nat_BG_VAT_Document_Type_VAT_Codes.md#document_type_vat_code_id)|
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
|Order|0|
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


Document type that generates VAT entries.


Document type that generates VAT entries.

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
|Derived From|[Nat_BG_VAT_Document_Type_VAT_Codes](Nat_BG_VAT_Document_Type_VAT_Codes.md).[Document_Type_Id](Nat_BG_VAT_Document_Type_VAT_Codes.md#document_type_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### VAT_Code


VAT_Code


VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values.


VAT code to use when creating VAT export files for the specified Document Type. Allowed values is government-regulated list of values.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Document_Type_VAT_Codes](Nat_BG_VAT_Document_Type_VAT_Codes.md).[VAT_Code](Nat_BG_VAT_Document_Type_VAT_Codes.md#vat_code)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Long|
|Supports EQUALS_IN|no|

### Cash_Reporting_VAT_Code


Cash_Reporting_VAT_Code


VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code.


VAT code, which will be used when Cash Reporting mode is used for the entry. Allowed values are the same as for VAT Code.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`01`, `02`, `03`, `04`, `05`, `07`, `09`, `11`, `12`, `13`, `81`, `82`, `91`, `92`, `93`, `94`|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Document_Type_VAT_Codes](Nat_BG_VAT_Document_Type_VAT_Codes.md).[Cash_Reporting_VAT_Code](Nat_BG_VAT_Document_Type_VAT_Codes.md#cash_reporting_vat_code)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


