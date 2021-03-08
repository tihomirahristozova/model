# Table Cms_News_Web_Modules

Represents a web module, containing news. Entity: Cms_News_Web_Modules

# Inheritance

* [Cms_Web_Modules](Cms_Web_Modules.md)

# Aggregate Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|News_Web_Module_Id|`Guid`|`PK`, Readonly||
|Is_Published|`Boolean`|||
|Local_Url|`String`|||
|Module_Picture|`Byte[]`|`BLOB`||
|Module_Type|`ModuleType`|Allowed: `CAT`, `STA`, `NEW`||
|Web_Module_Name|`String`|||
