# Table Nat_BG_VAT_Declarations

National data: Contains the VAT declarations, issued by the enterprise company, according to the Bulgarian legislation. Entity: Nat_BG_VAT_Declarations

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[VAT_Declaration_Id](#vat_declaration_id)|`uniqueidentifier` `PK`|Unique identification of the VAT declaration.|
|[Document_Id](#document_id)|`uniqueidentifier` ||
|[VAT_Period_Start](#vat_period_start)|`date` |Start date of the period fot which the VAT declaration is made.|
|[VAT_Period_End](#vat_period_end)|`date` |End date of the period fot which the VAT declaration is made.|
|[Declaring_Person_Id](#declaring_person_id)|`uniqueidentifier` |Specific declaring person for this declaration. If the declaring person isn't specified then the default declaring person for the enterprise company is used|
|[Coefficient_VATL_Article_73](#coefficient_vatl_article_73)|`decimal(3, 2)` |Field 01 - 33 from the declaration. Must be between 0.00 and 1.00.|
|[Deducted_VAT_Amount_Article_92_Paragraph_1](#deducted_vat_amount_article_92_paragraph_1)|`decimal(14, 2)` |Field 01 - 70 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[Deposited_VAT_Amount](#deposited_vat_amount)|`decimal(14, 2)` |Field 01 - 71 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Amount_To_Recoup_Article_92_Paragraph_1](#vat_amount_to_recoup_article_92_paragraph_1)|`decimal(14, 2)` |Field 01 - 80 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Amount_To_Recoup_Article_92_Paragraph_3](#vat_amount_to_recoup_article_92_paragraph_3)|`decimal(14, 2)` |Field 01 - 81 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Amount_To_Recoup_Article_92_Paragraph_4](#vat_amount_to_recoup_article_92_paragraph_4)|`decimal(14, 2)` |Field 01 - 82 from the declaration. Amounts are in base currency. Must be greater than 0.00.|
|[VAT_Declaration_Representing_Person_Id](#vat_declaration_representing_person_id)|`uniqueidentifier` |Representing person for the purposes of submitting of VAT declarations.|
|[VAT_Declaration_Representing_Person_Position](#vat_declaration_representing_person_position)|`nvarchar(64)` |Position of the representing person for the purposes of submitting of VAT declarations.|
|[Is_Single_Execution](#is_single_execution)|`bit` Readonly|Specifies whether the document is a single execution of its order document.|
|[Is_Released](#is_released)|`bit` Readonly|True if the document is not void and its state is released or greater|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### VAT_Declaration_Id


VAT_Declaration_Id


Unique identification of the VAT declaration.


Unique identification of the VAT declaration.

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
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Declaration_Id](Nat_BG_VAT_Declarations.md#vat_declaration_id)|
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

### Document_Id


Document_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Document_Id](Nat_BG_VAT_Declarations.md#document_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### VAT_Period_Start


VAT_Period_Start


Start date of the period fot which the VAT declaration is made.


Start date of the period fot which the VAT declaration is made.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Period_Start](Nat_BG_VAT_Declarations.md#vat_period_start)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### VAT_Period_End


VAT_Period_End


End date of the period fot which the VAT declaration is made.


End date of the period fot which the VAT declaration is made.

| Property | Value |
| - | - |
|Type|date|
|DateTime Format|Date|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Period_End](Nat_BG_VAT_Declarations.md#vat_period_end)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|yes|no|

### Declaring_Person_Id


Declaring_Person_Id


Specific declaring person for this declaration. If the declaring person isn't specified then the default declaring person for the enterprise company is used


Specific declaring person for this declaration. If the declaring person isn't specified then the default declaring person for the enterprise company is used

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Nat_BG_VAT_Declaring_Persons](Nat_BG_VAT_Declaring_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Declaring_Person_Id](Nat_BG_VAT_Declarations.md#declaring_person_id)|
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
|Visible|yes|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Coefficient_VATL_Article_73


Coefficient_VATL_Article_73


Field 01 - 33 from the declaration. Must be between 0.00 and 1.00.


Field 01 - 33 from the declaration. Must be between 0.00 and 1.00.

| Property | Value |
| - | - |
|Type|decimal(3, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Coefficient_VATL_Article_73](Nat_BG_VAT_Declarations.md#coefficient_vatl_article_73)|
|Format|N2|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

### Deducted_VAT_Amount_Article_92_Paragraph_1


Deducted_VAT_Amount_Article_92_Paragraph_1


Field 01 - 70 from the declaration. Amounts are in base currency. Must be greater than 0.00.


Field 01 - 70 from the declaration. Amounts are in base currency. Must be greater than 0.00.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Deducted_VAT_Amount_Article_92_Paragraph_1](Nat_BG_VAT_Declarations.md#deducted_vat_amount_article_92_paragraph_1)|
|Format|N2|
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

### Deposited_VAT_Amount


Deposited_VAT_Amount


Field 01 - 71 from the declaration. Amounts are in base currency. Must be greater than 0.00.


Field 01 - 71 from the declaration. Amounts are in base currency. Must be greater than 0.00.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Deposited_VAT_Amount](Nat_BG_VAT_Declarations.md#deposited_vat_amount)|
|Format|N2|
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

### VAT_Amount_To_Recoup_Article_92_Paragraph_1


VAT_Amount_To_Recoup_Article_92_Paragraph_1


Field 01 - 80 from the declaration. Amounts are in base currency. Must be greater than 0.00.


Field 01 - 80 from the declaration. Amounts are in base currency. Must be greater than 0.00.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Amount_To_Recoup_Article_92_Paragraph_1](Nat_BG_VAT_Declarations.md#vat_amount_to_recoup_article_92_paragraph_1)|
|Format|N2|
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

### VAT_Amount_To_Recoup_Article_92_Paragraph_3


VAT_Amount_To_Recoup_Article_92_Paragraph_3


Field 01 - 81 from the declaration. Amounts are in base currency. Must be greater than 0.00.


Field 01 - 81 from the declaration. Amounts are in base currency. Must be greater than 0.00.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Amount_To_Recoup_Article_92_Paragraph_3](Nat_BG_VAT_Declarations.md#vat_amount_to_recoup_article_92_paragraph_3)|
|Format|N2|
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

### VAT_Amount_To_Recoup_Article_92_Paragraph_4


VAT_Amount_To_Recoup_Article_92_Paragraph_4


Field 01 - 82 from the declaration. Amounts are in base currency. Must be greater than 0.00.


Field 01 - 82 from the declaration. Amounts are in base currency. Must be greater than 0.00.

| Property | Value |
| - | - |
|Type|decimal(14, 2)|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Amount_To_Recoup_Article_92_Paragraph_4](Nat_BG_VAT_Declarations.md#vat_amount_to_recoup_article_92_paragraph_4)|
|Format|N2|
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

### VAT_Declaration_Representing_Person_Id


VAT_Declaration_Representing_Person_Id


Representing person for the purposes of submitting of VAT declarations.


Representing person for the purposes of submitting of VAT declarations.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Declaration_Representing_Person_Id](Nat_BG_VAT_Declarations.md#vat_declaration_representing_person_id)|
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

### VAT_Declaration_Representing_Person_Position


VAT_Declaration_Representing_Person_Position


Position of the representing person for the purposes of submitting of VAT declarations.


Position of the representing person for the purposes of submitting of VAT declarations.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[VAT_Declaration_Representing_Person_Position](Nat_BG_VAT_Declarations.md#vat_declaration_representing_person_position)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Single_Execution


Is_Single_Execution


Specifies whether the document is a single execution of its order document.


Specifies whether the document is a single execution of its order document.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Is_Single_Execution](Nat_BG_VAT_Declarations.md#is_single_execution)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Is_Released


Is_Released


True if the document is not void and its state is released or greater


True if the document is not void and its state is released or greater

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Is_Released](Nat_BG_VAT_Declarations.md#is_released)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

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
|Derived From|[Nat_BG_VAT_Declarations](Nat_BG_VAT_Declarations.md).[Row_Version](Nat_BG_VAT_Declarations.md#row_version)|
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


