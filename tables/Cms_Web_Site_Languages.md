# Table Cms_Web_Site_Languages

Specifies a language, supported by the web site. Entity: Cms_Web_Site_Languages

# Aggregate Hierarchy

* [Cms_Web_Sites](Cms_Web_Sites.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Web_Site_Language_Id|`Guid`|`PK`, Readonly||
|Is_Active|`Boolean`||Specifies whether the support for the language is activated and should be published on the web. `Required` `Default(false)` |
|Language_Code|`String`||Two letter ISO language code. Sub-tags are currently not supported. `Required` |
|Notes|`String`||Notes for this WebSiteLanguage. |
