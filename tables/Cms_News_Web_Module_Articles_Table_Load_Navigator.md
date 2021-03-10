# Query Cms_News_Web_Module_Articles_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[News_Web_Module_Article_Id](#news_web_module_article_id)|`uniqueidentifier` `PK`||
|[News_Web_Module_Id](#news_web_module_id)|`uniqueidentifier` |The News Web Module, to which the current article is added.|
|[Author_Public_User_Id](#author_public_user_id)|`uniqueidentifier` |The author of the news article.|
|[Is_Published](#is_published)|`bit` |Specifies whether the article is published for display on web.|
|[Publish_Date](#publish_date)|`datetime` |The date and time when the news article should appear to be published.|
|[Language_Code](#language_code)|`nvarchar` |The language code of the article text.|
|[Article_Text_Html](#article_text_html)|`nvarchar` |The actual article text, stored as Html. Only the <BODY> of the Html is stored. The language of the text is specified in Language Code.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### News_Web_Module_Article_Id


News_Web_Module_Article_Id

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
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[News_Web_Module_Article_Id](Cms_News_Web_Module_Articles.md#news_web_module_article_id)|
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
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### News_Web_Module_Id


News_Web_Module_Id


The News Web Module, to which the current article is added.


The News Web Module, to which the current article is added.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cms_News_Web_Modules](Cms_News_Web_Modules.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[News_Web_Module_Id](Cms_News_Web_Module_Articles.md#news_web_module_id)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Author_Public_User_Id


Author_Public_User_Id


The author of the news article.


The author of the news article.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Ext_Public_Users](Ext_Public_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[Author_Public_User_Id](Cms_News_Web_Module_Articles.md#author_public_user_id)|
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
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Is_Published


Is_Published


Specifies whether the article is published for display on web.


Specifies whether the article is published for display on web.

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
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[Is_Published](Cms_News_Web_Module_Articles.md#is_published)|
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
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Publish_Date


Publish_Date


The date and time when the news article should appear to be published.


The date and time when the news article should appear to be published.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[Publish_Date](Cms_News_Web_Module_Articles.md#publish_date)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Language_Code


Language_Code


The language code of the article text.


The language code of the article text.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[Language_Code](Cms_News_Web_Module_Articles.md#language_code)|
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
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Article_Text_Html


Article_Text_Html


The actual article text, stored as Html. Only the <BODY> of the Html is stored. The language of the text is specified in Language Code.


The actual article text, stored as Html. Only the <BODY> of the Html is stored. The language of the text is specified in Language Code.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[Article_Text_Html](Cms_News_Web_Module_Articles.md#article_text_html)|
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
|Order|6|
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
|Derived From|[Cms_News_Web_Module_Articles](Cms_News_Web_Module_Articles.md).[Row_Version](Cms_News_Web_Module_Articles.md#row_version)|
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
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


