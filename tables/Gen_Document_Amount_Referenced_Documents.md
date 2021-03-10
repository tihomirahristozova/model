# Table Gen_Document_Amount_Referenced_Documents

Contains the documents which are referenced by each document amount. Entity: Gen_Document_Amount_Referenced_Documents

## Owner Tables Hierarchy

* [Gen_Document_Amounts](Gen_Document_Amounts.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Amount_Referenced_Document_Id](#document_amount_referenced_document_id)|`uniqueidentifier` `PK`||
|[Document_Amount_Id](#document_amount_id)|`uniqueidentifier` |The document amount for which the referenced document is specified.|
|[Referenced_Document_Id](#referenced_document_id)|`uniqueidentifier` |The document which is referenced by the document amount.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Amount_Referenced_Document_Id


Document_Amount_Referenced_Document_Id

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
|Derived From|[Gen_Document_Amount_Referenced_Documents](Gen_Document_Amount_Referenced_Documents.md).[Document_Amount_Referenced_Document_Id](Gen_Document_Amount_Referenced_Documents.md#document_amount_referenced_document_id)|
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

### Document_Amount_Id


Document_Amount_Id


The document amount for which the referenced document is specified.


The document amount for which the referenced document is specified.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Document_Amounts](Gen_Document_Amounts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Referenced_Documents](Gen_Document_Amount_Referenced_Documents.md).[Document_Amount_Id](Gen_Document_Amount_Referenced_Documents.md#document_amount_id)|
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
|Equals|NULL|no|no|

### Referenced_Document_Id


Referenced_Document_Id


The document which is referenced by the document amount.


The document which is referenced by the document amount.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Documents](Gen_Documents.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Amount_Referenced_Documents](Gen_Document_Amount_Referenced_Documents.md).[Referenced_Document_Id](Gen_Document_Amount_Referenced_Documents.md#referenced_document_id)|
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
|Derived From|[Gen_Document_Amount_Referenced_Documents](Gen_Document_Amount_Referenced_Documents.md).[Row_Version](Gen_Document_Amount_Referenced_Documents.md#row_version)|
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


