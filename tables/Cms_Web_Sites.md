# Table Cms_Web_Sites

Contains the public web sites. Entity: Cms_Web_Sites

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Web_Site_Id|`Guid`|`PK`, Readonly||
|Base_Url|`String`||The base url (address) of the web site. `Filter(like)` |
|Is_Published|`Boolean`||Specifies whether the site is published for public Internet access. `Required` `Default(false)` `Filter(eq)` |
|Web_Site_Name|`String`||Multilanguage web site name. `Required` `Filter(like)` |
