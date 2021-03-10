# Table Cms_Web_Modules

The abstract basic building block of web sites. Each module can render multiple web pages. Entity: Cms_Web_Modules

## Owner Tables Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Web_Module_Id](#web_module_id)|`uniqueidentifier` `PK`||
|[Web_Site_Id](#web_site_id)|`uniqueidentifier` |The web site to which the module belongs.|
|[Parent_Web_Module_Id](#parent_web_module_id)|`uniqueidentifier` |The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module.|
|[Web_Module_Name](#web_module_name)|`nvarchar(512)` |Multilanguage Module name. This is used as a title when displaying the web Module.|
|[Local_Url](#local_url)|`nvarchar(128)` |The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path.|
|[Is_Published](#is_published)|`bit` |Specifies whether the module is published and will be showed in the web site.|
|[Module_Picture](#module_picture)|`varbinary` |Default picture. Used for picture links, small module icons, etc. PNG format is suggested.|
|[Module_Type](#module_type)|`nvarchar(3)` Allowed: `CAT`, `STA`, `NEW`|Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Web_Module_Id


Web_Module_Id

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
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Web_Module_Id](Cms_Web_Modules.md#web_module_id)|
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

### Web_Site_Id


Web_Site_Id


The web site to which the module belongs.


The web site to which the module belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Cms_Web_Sites](Cms_Web_Sites.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Web_Site_Id](Cms_Web_Modules.md#web_site_id)|
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
|Equals|NULL|no|no|

### Parent_Web_Module_Id


Parent_Web_Module_Id


The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module.


The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cms_Web_Modules](Cms_Web_Modules.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Parent_Web_Module_Id](Cms_Web_Modules.md#parent_web_module_id)|
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

### Web_Module_Name


Web_Module_Name


Multilanguage Module name. This is used as a title when displaying the web Module.


Multilanguage Module name. This is used as a title when displaying the web Module.

| Property | Value |
| - | - |
|Type|nvarchar(512)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Web_Module_Name](Cms_Web_Modules.md#web_module_name)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Local_Url


Local_Url


The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path.


The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Local_Url](Cms_Web_Modules.md#local_url)|
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
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Is_Published


Is_Published


Specifies whether the module is published and will be showed in the web site.


Specifies whether the module is published and will be showed in the web site.

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
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Is_Published](Cms_Web_Modules.md#is_published)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Module_Picture


Module_Picture


Default picture. Used for picture links, small module icons, etc. PNG format is suggested.


Default picture. Used for picture links, small module icons, etc. PNG format is suggested.

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
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Module_Picture](Cms_Web_Modules.md#module_picture)|
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

### Module_Type


Module_Type


Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc.


Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc.

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
|Allowed Values|`CAT`, `STA`, `NEW`|
|Default Value|None|
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Module_Type](Cms_Web_Modules.md#module_type)|
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
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

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
|Derived From|[Cms_Web_Modules](Cms_Web_Modules.md).[Row_Version](Cms_Web_Modules.md#row_version)|
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


