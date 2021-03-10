# Table Gen_Document_Print_Images

Contains the data of a printout of a document as it was obtained from the data source in the moment of printing. Entity: Gen_Document_Print_Images

## Owner Tables Hierarchy

* [Gen_Printout_Layouts](Gen_Printout_Layouts.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Document_Print_Image_Id](#document_print_image_id)|`uniqueidentifier` `PK`||
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` |The print layout, which was used for the current printout.|
|[Print_Image_Format](#print_image_format)|`nvarchar(3)` |The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported.|
|[Print_Image](#print_image)|`varbinary` |The data of the printout, stored in the format, specified in Print Image Format.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Document_Print_Image_Id


Document_Print_Image_Id

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
|Derived From|[Gen_Document_Print_Images](Gen_Document_Print_Images.md).[Document_Print_Image_Id](Gen_Document_Print_Images.md#document_print_image_id)|
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

### Printout_Layout_Id


Printout_Layout_Id


The print layout, which was used for the current printout.


The print layout, which was used for the current printout.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Gen_Printout_Layouts](Gen_Printout_Layouts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Print_Images](Gen_Document_Print_Images.md).[Printout_Layout_Id](Gen_Document_Print_Images.md#printout_layout_id)|
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

### Print_Image_Format


Print_Image_Format


The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported.


The format, which is used to represent the print image. Currently, only 'CDS' = Compressed Data Set is supported.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CDS|
|Derived From|[Gen_Document_Print_Images](Gen_Document_Print_Images.md).[Print_Image_Format](Gen_Document_Print_Images.md#print_image_format)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|no|

### Print_Image


Print_Image


The data of the printout, stored in the format, specified in Print Image Format.


The data of the printout, stored in the format, specified in Print Image Format.

| Property | Value |
| - | - |
|Type|varbinary|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Document_Print_Images](Gen_Document_Print_Images.md).[Print_Image](Gen_Document_Print_Images.md#print_image)|
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
|Derived From|[Gen_Document_Print_Images](Gen_Document_Print_Images.md).[Row_Version](Gen_Document_Print_Images.md#row_version)|
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


