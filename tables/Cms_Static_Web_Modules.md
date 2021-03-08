# Table Cms_Static_Web_Modules

A web module, which contains one web page with static text. Entity: Cms_Static_Web_Modules

# Inheritance

* [Cms_Web_Modules](Cms_Web_Modules.md)

# Aggregate Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Static_Web_Module_Id|`Guid`|`PK`, Readonly||
|Content_Html|`String`||The actual html content of the pade. Only the <BODY> of the html is stored. |
|Is_Published|`Boolean`|||
|Language_Code|`String`||The language code of the content. `Required` `Default("EN")` |
|Local_Url|`String`|||
|Module_Picture|`Byte[]`|`BLOB`||
|Module_Type|`ModuleType`|Allowed: `CAT`, `STA`, `NEW`||
|Web_Module_Name|`String`|||
