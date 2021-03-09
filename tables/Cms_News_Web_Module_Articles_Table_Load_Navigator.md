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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### News_Web_Module_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Author_Public_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Is_Published

| Property | Value |
| - | - |
|Type|bit|

### Publish_Date

| Property | Value |
| - | - |
|Type|datetime|

### Language_Code

| Property | Value |
| - | - |
|Type|nvarchar|

### Article_Text_Html

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


