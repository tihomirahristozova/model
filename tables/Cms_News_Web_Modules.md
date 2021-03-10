# Table Cms_News_Web_Modules

Represents a web module, containing news. Entity: Cms_News_Web_Modules

## Owner Tables Hierarchy

* [Cms_Web_Modules](Cms_Web_Modules.md)
* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[News_Web_Module_Id](#news_web_module_id)|`uniqueidentifier` `PK`||
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` |The web module, which this News Module inherits.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### News_Web_Module_Id


News_Web_Module_Id

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
|Derived From|[Cms_News_Web_Modules](Cms_News_Web_Modules.md).[News_Web_Module_Id](Cms_News_Web_Modules.md#news_web_module_id)|
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

### Web_Module_Id


Web_Module_Id


The web module, which this News Module inherits.


The web module, which this News Module inherits.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cms_Web_Modules](Cms_Web_Modules.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_News_Web_Modules](Cms_News_Web_Modules.md).[Web_Module_Id](Cms_News_Web_Modules.md#web_module_id)|
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
|Derived From|[Cms_News_Web_Modules](Cms_News_Web_Modules.md).[Row_Version](Cms_News_Web_Modules.md#row_version)|
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


