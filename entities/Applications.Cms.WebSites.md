# Applications.Cms.WebSites

Contains the public web sites. Entity: Cms_Web_Sites

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Cms.WebSites.md#Id) | guid |  
| [BaseUrl](Applications.Cms.WebSites.md#BaseUrl) | string (nullable) | The base url (address) of the web site. [Filter(like)] 
| [IsPublished](Applications.Cms.WebSites.md#IsPublished) | boolean | Specifies whether the site is published for public Internet access. [Required] [Default(false)] [Filter(eq)] 
| [Name](Applications.Cms.WebSites.md#Name) | string | Multilanguage web site name. [Required] [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Applications.Cms.WebSites.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company to which this web site belongs. [Required] [Filter(multi eq)] |
| [PublicUserList](Applications.Cms.WebSites.md#PublicUserList) | [Systems.External.PublicUserLists](Systems.External.PublicUserLists.md) (nullable) | The list of users used to authorize the users on the site. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| WebModules | [Applications.Cms.WebModules](Applications.Cms.WebModules.md) | List of [WebModule](Applications.Cms.WebModules.md) child objects, based on the [Applications.Cms.WebModule.WebSite](Applications.Cms.WebModules.md#WebSite) back reference 
| Languages | [Applications.Cms.WebSiteLanguages](Applications.Cms.WebSiteLanguages.md) | List of [WebSiteLanguage](Applications.Cms.WebSiteLanguages.md) child objects, based on the [Applications.Cms.WebSiteLanguage.WebSite](Applications.Cms.WebSiteLanguages.md#WebSite) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### BaseUrl

> The base url (address) of the web site. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### IsPublished

> Specifies whether the site is published for public Internet access. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

> Multilanguage web site name. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company to which this web site belongs. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PublicUserList

> The list of users used to authorize the users on the site. [Filter(multi eq)]

_Type_: **[Systems.External.PublicUserLists](Systems.External.PublicUserLists.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Cms.WebSites erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Cms.WebSites erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Cms.WebSites erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Cms_WebSites?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Cms_WebSites?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cms_Web_Sites?$top=10>

