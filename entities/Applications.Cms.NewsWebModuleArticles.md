---
uid: Applications.Cms.NewsWebModuleArticles
---
# Applications.Cms.NewsWebModuleArticles

Represents an article in a news web module. Entity: Cms_News_Web_Module_Articles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Cms.NewsWebModuleArticles.md#Id) | guid |  
| [ArticleTextHtml](Applications.Cms.NewsWebModuleArticles.md#ArticleTextHtml) | string (nullable) | The actual article text, stored as Html. Only the <BODY> of the Html is stored. The language of the text is specified in Language Code. 
| [IsPublished](Applications.Cms.NewsWebModuleArticles.md#IsPublished) | boolean | Specifies whether the article is published for display on web. [Required] [Default(false)] 
| [LanguageCode](Applications.Cms.NewsWebModuleArticles.md#LanguageCode) | string | The language code of the article text. [Required] 
| [PublishDate](Applications.Cms.NewsWebModuleArticles.md#PublishDate) | datetime | The date and time when the news article should appear to be published. [Required] [Default(Now)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AuthorPublicUser](Applications.Cms.NewsWebModuleArticles.md#AuthorPublicUser) | [Systems.External.PublicUsers](Systems.External.PublicUsers.md) | The author of the news article. [Required] [Filter(multi eq)] |
| [NewsWebModule](Applications.Cms.NewsWebModuleArticles.md#NewsWebModule) | [Applications.Cms.NewsWebModules](Applications.Cms.NewsWebModules.md) | The News Web Module, to which the current article is added. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ArticleTextHtml

> The actual article text, stored as Html. Only the <BODY> of the Html is stored. The language of the text is specified in Language Code.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsPublished

> Specifies whether the article is published for display on web. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LanguageCode

> The language code of the article text. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PublishDate

> The date and time when the news article should appear to be published. [Required] [Default(Now)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  


## Reference Details

### AuthorPublicUser

> The author of the news article. [Required] [Filter(multi eq)]

_Type_: **[Systems.External.PublicUsers](Systems.External.PublicUsers.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### NewsWebModule

> The News Web Module, to which the current article is added. [Required] [Filter(multi eq)]

_Type_: **[Applications.Cms.NewsWebModules](Applications.Cms.NewsWebModules.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Cms.NewsWebModuleArticles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Cms.NewsWebModuleArticles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Cms.NewsWebModuleArticles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Cms_NewsWebModuleArticles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Cms_NewsWebModuleArticles?$top=10>

