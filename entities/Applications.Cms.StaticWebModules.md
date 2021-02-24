---
uid: Applications.Cms.StaticWebModules
---
# Applications.Cms.StaticWebModules Entity

**Namespace:** [Applications.Cms](Applications.Cms.md)  
**Inherited From:** [Applications.Cms.WebModules](Applications.Cms.WebModules.md)  

A web module, which contains one web page with static text. Entity: Cms_Static_Web_Modules

## Default Visualization
Default Display Text Format:  
_{LanguageCode}: {Name:T}_  
Default Search Member:  
_LanguageCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Cms.WebSites](Applications.Cms.WebSites.md)  
Aggregate Root:  
[Applications.Cms.WebSites](Applications.Cms.WebSites.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContentHtml](Applications.Cms.StaticWebModules.md#contenthtml) | string (nullable) | The actual html content of the pade. Only the <BODY> of the html is stored. 
| [Id](Applications.Cms.StaticWebModules.md#id) | guid |  
| [IsPublished](Applications.Cms.StaticWebModules.md#ispublished) | boolean | Specifies whether the module is published and will be showed in the web site. [Required] [Default(false)] [Filter(eq)] (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [LanguageCode](Applications.Cms.StaticWebModules.md#languagecode) | string | The language code of the content. [Required] [Default("EN")] 
| [LocalUrl](Applications.Cms.StaticWebModules.md#localurl) | string (nullable) | The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path. [Filter(like)] (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [ModulePicture](Applications.Cms.StaticWebModules.md#modulepicture) | byte[] (nullable) | Default picture. Used for picture links, small module icons, etc. PNG format is suggested. (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [ModuleType](Applications.Cms.StaticWebModules.md#moduletype) | [ModuleType](Applications.Cms.StaticWebModules.md#moduletype) | Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc. [Required] [Filter(like)] (Inherited from [WebModules](Applications.Cms.WebModules.md)) 
| [Name](Applications.Cms.StaticWebModules.md#name) | string | Multilanguage Module name. This is used as a title when displaying the web Module. [Required] [Filter(like)] (Inherited from [WebModules](Applications.Cms.WebModules.md)) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.Cms.StaticWebModules.md#parent) | [WebModules](Applications.Cms.WebModules.md) (nullable) | The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module. [Filter(multi eq)] (Inherited from [WebModules](Applications.Cms.WebModules.md)) |
| [WebSite](Applications.Cms.StaticWebModules.md#website) | [WebSites](Applications.Cms.WebSites.md) | The web site to which the module belongs. [Required] [Filter(multi eq)] [Owner] (Inherited from [WebModules](Applications.Cms.WebModules.md)) |


## Attribute Details

### ContentHtml

The actual html content of the pade. Only the <BODY> of the html is stored.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsPublished

Specifies whether the module is published and will be showed in the web site. [Required] [Default(false)] [Filter(eq)] (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LanguageCode

The language code of the content. [Required] [Default("EN")]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **EN**  

### LocalUrl

The local Module Url. The full Url of a module is formed based on the sites Base Url, the local Urls of all parent modules and the module Local Url. Null means that the web Module is the default web module within the parent path. [Filter(like)] (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ModulePicture

Default picture. Used for picture links, small module icons, etc. PNG format is suggested. (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ModuleType

Specifies the content handler. The content handler is responsible for generating the actual web page content. Module Types include Category, Static, News, Product, etc. [Required] [Filter(like)] (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **[ModuleType](Applications.Cms.StaticWebModules.md#moduletype)**  
Allowed values for the [ModuleType](Applications.Cms.WebModules.md#moduletype) data attribute  
_Allowed Values (Applications.Cms.WebModulesRepository.ModuleType Enum Members)_  

| Value | Description |
| ---- | --- |
| CategoryPage | CategoryPage value. Stored as 'CAT'. <br /> _Database Value:_ 'CAT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'CategoryPage' |
| Static | Static value. Stored as 'STA'. <br /> _Database Value:_ 'STA' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Static' |
| News | News value. Stored as 'NEW'. <br /> _Database Value:_ 'NEW' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'News' |

_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Name

Multilanguage Module name. This is used as a title when displaying the web Module. [Required] [Filter(like)] (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### Parent

The parent web Module. It can only be a module with Module Type = Category. Null means that the web Module is root web Module. [Filter(multi eq)] (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **[WebModules](Applications.Cms.WebModules.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### WebSite

The web site to which the module belongs. [Required] [Filter(multi eq)] [Owner] (Inherited from [WebModules](Applications.Cms.WebModules.md))

_Type_: **[WebSites](Applications.Cms.WebSites.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Cms.StaticWebModules erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Cms.StaticWebModules erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Cms_StaticWebModules?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Cms_StaticWebModules?$top=10>

