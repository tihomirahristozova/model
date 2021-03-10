# Table Gen_Document_Versions

History of each saved version of each document. Entity: Gen_Document_Versions

## Owner Tables Hierarchy

* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Version_Id](#document_version_id)|`uniqueidentifier` `PK`||
|[Document_Id](#document_id)|`uniqueidentifier` |The document whoose version is stored in this row|
|[Version](#version)|`int` Readonly|The version number that is stored in this row|
|[Document_Data_XML](#document_data_xml)|`nvarchar(2147483647)` |The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed).|
|[Update_Time](#update_time)|`datetime` Readonly|The date and time when this version was saved|
|[Update_User](#update_user)|`nvarchar(64)` Readonly|The login name of the user that saved this version|
|[State](#state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`, `5`, Readonly|The state of the document by the time it was saved|
|[Document_Data_Format](#document_data_format)|`nvarchar(1)` |The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data.|
|[Document_Data](#document_data)|`varbinary` |Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed).|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Version_Id


Document_Version_Id

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
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Document_Version_Id](Gen_Document_Versions.md#document_version_id)|
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

### Document_Id


Document_Id


The document whoose version is stored in this row


The document whoose version is stored in this row

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
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Document_Id](Gen_Document_Versions.md#document_id)|
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

### Version


Version


The version number that is stored in this row


The version number that is stored in this row

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Version](Gen_Document_Versions.md#version)|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|
|GreaterThanOrLessThan|None|yes|no|

### Document_Data_XML


Document_Data_XML


The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed).


The uncompressed XML representation of the document data, including the document row, the header row and all types of lines. Valid when Document Data Format = U (uncompressed).

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
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Document_Data_XML](Gen_Document_Versions.md#document_data_xml)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Update_Time


Update_Time


The date and time when this version was saved


The date and time when this version was saved

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|yes|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Update_Time](Gen_Document_Versions.md#update_time)|
|Format|g|
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
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|GreaterThanOrLessThan|None|no|no|

### Update_User


Update_User


The login name of the user that saved this version


The login name of the user that saved this version

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Update_User](Gen_Document_Versions.md#update_user)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|yes|
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
|Like|None|no|no|

### State


State


The state of the document by the time it was saved


The state of the document by the time it was saved

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `10`, `20`, `30`, `40`, `50`, `5`|
|Default Value|0|
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[State](Gen_Document_Versions.md#state)|
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

### Document_Data_Format


Document_Data_Format


The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data.


The format of the saved document data. 'U' - uncompressed and stored in Document Data XML; 'D' - Deflate compressed and stored in Document Data.

| Property | Value |
| - | - |
|Type|nvarchar(1)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|U|
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Document_Data_Format](Gen_Document_Versions.md#document_data_format)|
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
|Max Length|1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Document_Data


Document_Data


Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed).


Compressed representation of the document data. Valid when Document Data Format = D (deflate compressed).

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
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Document_Data](Gen_Document_Versions.md#document_data)|
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
|Derived From|[Gen_Document_Versions](Gen_Document_Versions.md).[Row_Version](Gen_Document_Versions.md#row_version)|
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


