---
uid: Applications.Cms.WebSiteLanguages
---
# Applications.Cms.WebSiteLanguages Entity

Specifies a language, supported by the web site. Entity: Cms_Web_Site_Languages

Default Display Text Format:  
_{LanguageCode}_  
Default Search Member:  
_LanguageCode_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Cms.WebSiteLanguages.md#id) | guid |  
| [IsActive](Applications.Cms.WebSiteLanguages.md#isactive) | boolean | Specifies whether the support for the language is activated and should be published on the web. [Required] [Default(false)] 
| [LanguageCode](Applications.Cms.WebSiteLanguages.md#languagecode) | string | Two letter ISO language code. Sub-tags are currently not supported. [Required] 
| [Notes](Applications.Cms.WebSiteLanguages.md#notes) | string (nullable) | Notes for this WebSiteLanguage. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [WebSite](Applications.Cms.WebSiteLanguages.md#website) | [WebSites](Applications.Cms.WebSites.md) | The web site, for which the language is specified. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the support for the language is activated and should be published on the web. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LanguageCode

Two letter ISO language code. Sub-tags are currently not supported. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this WebSiteLanguage.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### WebSite

The web site, for which the language is specified. [Required] [Filter(multi eq)] [Owner]

_Type_: **[WebSites](Applications.Cms.WebSites.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Cms.WebSiteLanguages erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Cms.WebSiteLanguages erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Cms_WebSiteLanguages?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Cms_WebSiteLanguages?$top=10>

