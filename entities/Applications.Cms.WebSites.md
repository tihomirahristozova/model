---
uid: Applications.Cms.WebSites
---
# Applications.Cms.WebSites Entity

**Namespace:** [Applications.Cms](Applications.Cms.md)  

Contains the public web sites. Entity: Cms_Web_Sites

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Cms.WebSites](Applications.Cms.WebSites.md)  
  * [Applications.Cms.NewsWebModules](Applications.Cms.NewsWebModules.md)  
  * [Applications.Cms.ProductCatalogWebModules](Applications.Cms.ProductCatalogWebModules.md)  
  * [Applications.Cms.StaticWebModules](Applications.Cms.StaticWebModules.md)  
  * [Applications.Cms.WebModules](Applications.Cms.WebModules.md)  
  * [Applications.Cms.WebSiteLanguages](Applications.Cms.WebSiteLanguages.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [BaseUrl](Applications.Cms.WebSites.md#baseurl) | string (256) __nullable__ | The base url (address) of the web site. `Filter(like)` 
| [Id](Applications.Cms.WebSites.md#id) | guid |  
| [IsPublished](Applications.Cms.WebSites.md#ispublished) | boolean | Specifies whether the site is published for public Internet access. `Required` `Default(false)` `Filter(eq)` 
| [Name](Applications.Cms.WebSites.md#name) | string (256) | Multilanguage web site name. `Required` `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.Cms.WebSites.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company to which this web site belongs. `Required` `Filter(multi eq)` |
| [PublicUserList](Applications.Cms.WebSites.md#publicuserlist) | [PublicUserLists](Systems.External.PublicUserLists.md) (nullable) | The list of users used to authorize the users on the site. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Languages | [WebSiteLanguages](Applications.Cms.WebSiteLanguages.md) | List of `WebSiteLanguage`(Applications.Cms.WebSiteLanguages.md) child objects, based on the `Applications.Cms.WebSiteLanguage.WebSite`(Applications.Cms.WebSiteLanguages.md#website) back reference 
| WebModules | [WebModules](Applications.Cms.WebModules.md) | List of WebModule child objects, based on the Applications.Cms.WebModule.WebSite back reference 


## Attribute Details

### BaseUrl

The base url (address) of the web site. `Filter(like)`

_Type_: **string (256) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsPublished

Specifies whether the site is published for public Internet access. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

Multilanguage web site name. `Required` `Filter(like)`

_Type_: **string (256)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  


## Reference Details

### EnterpriseCompany

The enterprise company to which this web site belongs. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### PublicUserList

The list of users used to authorize the users on the site. `Filter(multi eq)`

_Type_: **[PublicUserLists](Systems.External.PublicUserLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Cms.WebSites erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Cms.WebSites erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Cms_WebSites?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Cms_WebSites?$top=10>

