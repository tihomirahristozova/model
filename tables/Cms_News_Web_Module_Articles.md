# Table Cms_News_Web_Module_Articles

Represents an article in a news web module. Entity: Cms_News_Web_Module_Articles

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|News_Web_Module_Article_Id|`Guid`|`PK`, Readonly||
|Article_Text_Html|`String`||The actual article text, stored as Html. Only the <BODY> of the Html is stored. The language of the text is specified in Language Code. |
|Is_Published|`Boolean`||Specifies whether the article is published for display on web. `Required` `Default(false)` |
|Language_Code|`String`||The language code of the article text. `Required` |
|Publish_Date|`DateTime`||The date and time when the news article should appear to be published. `Required` `Default(Now)` |
