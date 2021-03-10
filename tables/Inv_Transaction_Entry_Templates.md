# Table Inv_Transaction_Entry_Templates

Obsolete. Not used. Entity: Inv_Transaction_Entry_Templates

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transaction_Entry_Template_Id](#transaction_entry_template_id)|`uniqueidentifier` `PK`||
|[Route_Id](#route_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Deal_Type_Id](#deal_type_id)|`uniqueidentifier` |Obsolete. Not used.|
|[Document_Notes_Fixed_Text](#document_notes_fixed_text)|`nvarchar(2147483647)` |Specifies the text for the document notes in the created entry in the VAT ledgers, in case the source is set to be fixed text.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Transaction_Entry_Template_Id


Transaction_Entry_Template_Id

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
|Derived From|[Inv_Transaction_Entry_Templates](Inv_Transaction_Entry_Templates.md).[Transaction_Entry_Template_Id](Inv_Transaction_Entry_Templates.md#transaction_entry_template_id)|
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

### Route_Id


Route_Id


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Wf_Routes](Wf_Routes.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Transaction_Entry_Templates](Inv_Transaction_Entry_Templates.md).[Route_Id](Inv_Transaction_Entry_Templates.md#route_id)|
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

### Deal_Type_Id


Deal_Type_Id


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[VAT_Deal_Types](VAT_Deal_Types.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Inv_Transaction_Entry_Templates](Inv_Transaction_Entry_Templates.md).[Deal_Type_Id](Inv_Transaction_Entry_Templates.md#deal_type_id)|
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
|UI Width|Long|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Document_Notes_Fixed_Text


Document_Notes_Fixed_Text


Specifies the text for the document notes in the created entry in the VAT ledgers, in case the source is set to be fixed text.


Specifies the text for the document notes in the created entry in the VAT ledgers, in case the source is set to be fixed text.

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
|Derived From|[Inv_Transaction_Entry_Templates](Inv_Transaction_Entry_Templates.md).[Document_Notes_Fixed_Text](Inv_Transaction_Entry_Templates.md#document_notes_fixed_text)|
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
|Derived From|[Inv_Transaction_Entry_Templates](Inv_Transaction_Entry_Templates.md).[Row_Version](Inv_Transaction_Entry_Templates.md#row_version)|
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


