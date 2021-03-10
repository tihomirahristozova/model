# Table Cms_Static_Web_Modules

A web module, which contains one web page with static text. Entity: Cms_Static_Web_Modules

## Owner Tables Hierarchy

* [Cms_Web_Modules](Cms_Web_Modules.md)
* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Static_Web_Module_Id](#static_web_module_id)|`uniqueidentifier` `PK`||
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` |The web module, which is inherited by this static module.|
|[Language_Code](#language_code)|`nvarchar(7)` |The language code of the content.|
|[Content_Html](#content_html)|`nvarchar(2147483647)` |The actual html content of the pade. Only the <BODY> of the html is stored.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Static_Web_Module_Id


Static_Web_Module_Id

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
|Derived From|[Cms_Static_Web_Modules](Cms_Static_Web_Modules.md).[Static_Web_Module_Id](Cms_Static_Web_Modules.md#static_web_module_id)|
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


The web module, which is inherited by this static module.


The web module, which is inherited by this static module.

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
|Derived From|[Cms_Static_Web_Modules](Cms_Static_Web_Modules.md).[Web_Module_Id](Cms_Static_Web_Modules.md#web_module_id)|
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

### Language_Code


Language_Code


The language code of the content.


The language code of the content.

| Property | Value |
| - | - |
|Type|nvarchar(7)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|EN|
|Derived From|[Cms_Static_Web_Modules](Cms_Static_Web_Modules.md).[Language_Code](Cms_Static_Web_Modules.md#language_code)|
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
|Max Length|7|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Content_Html


Content_Html


The actual html content of the pade. Only the <BODY> of the html is stored.


The actual html content of the pade. Only the <BODY> of the html is stored.

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
|Derived From|[Cms_Static_Web_Modules](Cms_Static_Web_Modules.md).[Content_Html](Cms_Static_Web_Modules.md#content_html)|
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
|Derived From|[Cms_Static_Web_Modules](Cms_Static_Web_Modules.md).[Row_Version](Cms_Static_Web_Modules.md#row_version)|
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


