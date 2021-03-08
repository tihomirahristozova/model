# Table Cms_Web_Modules

The abstract basic building block of web sites. Each module can render multiple web pages. Entity: Cms_Web_Modules

# Aggregate Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Web_Module_Id|`Guid`|`PK`, Readonly||
|Is_Published|`Boolean`||Specifies whether the module is published and will be showed in the web site. `Required` `Default(false)` `Filter(eq)` |
|Local_Url|`String`||The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path. `Filter(like)` |
|Module_Picture|`Byte[]`|`BLOB`|Default picture. Used for picture links, small module icons, etc. PNG format is suggested. |
|Module_Type|`ModuleType`|Allowed: `CAT`, `STA`, `NEW`|Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc. `Required` `Filter(like)` |
|Web_Module_Name|`String`||Multilanguage Module name. This is used as a title when displaying the web Module. `Required` `Filter(like)` |
