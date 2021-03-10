# Table Gen_Printouts

Contains data about binding of printout layouts to specific user-defined document types. Entity: Gen_Printouts

## Owner Tables Hierarchy

* [Gen_Document_Types](Gen_Document_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Printout_Id](#printout_id)|`uniqueidentifier` `PK`||
|[Application_Name](#application_name)|`nvarchar(64)` |The application which stored and uses the printout|
|[Printout_Name](#printout_name)|`nvarchar(64)` |The name of the printout. Unique within the application form|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Document_Type_Id](#document_type_id)|`uniqueidentifier` |The document type to which this printout layout is bound.|
|[Printout_Layout_Id](#printout_layout_id)|`uniqueidentifier` |The printout layout, that is bound to the document type.|
|[Definition_Format](#definition_format)|`nvarchar(16)` |Obsolete. Not used.|
|[Definition](#definition)|`nvarchar(1073741823)` |Obsolete. Not used.|
|[Is_Default](#is_default)|`bit` |1 if this is the default printout for the application form|
|[Ord](#ord)|`int` |Order in the list of printouts when using direct printing|
|[Copies](#copies)|`int` |Number of copies that should be printed when using direct printing|
|[Report_Id](#report_id)|`uniqueidentifier` |If not NULL points to a custom report that indicates which data will be loaded in the printout.|
|[Backward_Compatibility](#backward_compatibility)|`bit` |Obsolete. Not used.|
|[Allow_Printing_On_State](#allow_printing_on_state)|`smallint` Allowed: `0`, `10`, `20`, `30`, `40`, `50`|The user can print documents only with state equal or greater than Allow_Printing_On_State|
|[Ord_Priority](#ord_priority)|`int` |Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command.|
|[Ord_Filter_Xml](#ord_filter_xml)|`nvarchar(2147483647)` |The condition, required to be matched in order for the printout to be executed upon "Print All" command.|
|[Notes](#notes)|`nvarchar(512)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Printout_Id


Printout_Id

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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Printout_Id](Gen_Printouts.md#printout_id)|
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

### Application_Name


Application_Name


The application which stored and uses the printout


The application which stored and uses the printout

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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Application_Name](Gen_Printouts.md#application_name)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Printout_Name


Printout_Name


The name of the printout. Unique within the application form


The name of the printout. Unique within the application form

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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Printout_Name](Gen_Printouts.md#printout_name)|
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
|UI Width|Long|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Enterprise_Company_Id


Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Enterprise_Companies](Gen_Enterprise_Companies.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Enterprise_Company_Id](Gen_Printouts.md#enterprise_company_id)|
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

### Document_Type_Id


Document_Type_Id


The document type to which this printout layout is bound.


The document type to which this printout layout is bound.

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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Document_Type_Id](Gen_Printouts.md#document_type_id)|
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

### Printout_Layout_Id


Printout_Layout_Id


The printout layout, that is bound to the document type.


The printout layout, that is bound to the document type.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Gen_Printout_Layouts](Gen_Printout_Layouts.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Printout_Layout_Id](Gen_Printouts.md#printout_layout_id)|
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

### Definition_Format


Definition_Format


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|nvarchar(16)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|default|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Definition_Format](Gen_Printouts.md#definition_format)|
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
|Max Length|16|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Definition


Definition


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|nvarchar(1073741823)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Definition](Gen_Printouts.md#definition)|
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
|Max Length|1073741823|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Default


Is_Default


1 if this is the default printout for the application form


1 if this is the default printout for the application form

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Is_Default](Gen_Printouts.md#is_default)|
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
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Ord


Ord


Order in the list of printouts when using direct printing


Order in the list of printouts when using direct printing

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Ord](Gen_Printouts.md#ord)|
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

### Copies


Copies


Number of copies that should be printed when using direct printing


Number of copies that should be printed when using direct printing

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|1|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Copies](Gen_Printouts.md#copies)|
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

### Report_Id


Report_Id


If not NULL points to a custom report that indicates which data will be loaded in the printout.


If not NULL points to a custom report that indicates which data will be loaded in the printout.

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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Report_Id](Gen_Printouts.md#report_id)|
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
|Equals|NULL|yes|no|

### Backward_Compatibility


Backward_Compatibility


Obsolete. Not used.


Obsolete. Not used.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Backward_Compatibility](Gen_Printouts.md#backward_compatibility)|
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

### Allow_Printing_On_State


Allow_Printing_On_State


The user can print documents only with state equal or greater than Allow_Printing_On_State


The user can print documents only with state equal or greater than Allow_Printing_On_State

| Property | Value |
| - | - |
|Type|smallint|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`0`, `10`, `20`, `30`, `40`, `50`|
|Default Value|0|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Allow_Printing_On_State](Gen_Printouts.md#allow_printing_on_state)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Ord_Priority


Ord_Priority


Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command.


Ordinal position and priority of the printout, in regard to other printouts within the current document type. Used for sorting, when executing printouts with "Print All" command.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Ord_Priority](Gen_Printouts.md#ord_priority)|
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

### Ord_Filter_Xml


Ord_Filter_Xml


The condition, required to be matched in order for the printout to be executed upon "Print All" command.


The condition, required to be matched in order for the printout to be executed upon "Print All" command.

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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Ord_Filter_Xml](Gen_Printouts.md#ord_filter_xml)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|yes|
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

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(512)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Notes](Gen_Printouts.md#notes)|
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
|Max Length|512|
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
|Derived From|[Gen_Printouts](Gen_Printouts.md).[Row_Version](Gen_Printouts.md#row_version)|
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


