---
uid: Systems.Core.WebSites
---
# Systems.Core.WebSites

Contains the web sites, which are hosted for the database. Entity: Sys_Web_Sites (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.WebSites.md#Id) | guid |  
| [IsActive](Systems.Core.WebSites.md#IsActive) | boolean | Indicates whether the web site is active and will be instantiated upon next web server restart. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Systems.Core.WebSites.md#Notes) | string (nullable) | Notes for this WebSite. 
| [RelativeUrl](Systems.Core.WebSites.md#RelativeUrl) | string (nullable) | The relative Url of the site. This is the text after the first slash after the protocol and host name. The text should not include the protocol and host name. null means that the site will be hosted as the root site in the speicified web host. 
| [WebSiteType](Systems.Core.WebSites.md#WebSiteType) | [Systems.Core.WebSitesRepository.WebSiteType](Systems.Core.WebSites.md#WebSiteType) | The type of web site - Api, Client Center, Id, etc. [Required] [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Systems.Core.WebSites.md#EnterpriseCompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The enterprise company, for which is the site. null means, that the web site should not be enterprise company specific. [Filter(multi eq)] |
| [TrustedApplication](Systems.Core.WebSites.md#TrustedApplication) | [Systems.Security.TrustedApplications](Systems.Security.TrustedApplications.md) (nullable) | The trusted application related to this web site. [Filter(multi eq)] (Introduced in version 20.1.100.0) |
| [WebHost](Systems.Core.WebSites.md#WebHost) | [Systems.Core.WebHosts](Systems.Core.WebHosts.md) (nullable) | The web host in which to host the site. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates whether the web site is active and will be instantiated upon next web server restart. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this WebSite.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### RelativeUrl

> The relative Url of the site. This is the text after the first slash after the protocol and host name. The text should not include the protocol and host name. null means that the site will be hosted as the root site in the speicified web host.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### WebSiteType

> The type of web site - Api, Client Center, Id, etc. [Required] [Filter(multi eq)]

_Type_: **[Systems.Core.WebSitesRepository.WebSiteType](Systems.Core.WebSites.md#WebSiteType)**  
Allowed values for the [WebSiteType](Systems.Core.WebSites.md#WebSiteType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| API | API value. Stored as 'API'. <br /> _Database Value:_ 'API' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'API' |
| ClientCenter | ClientCenter value. Stored as 'CC'. <br /> _Database Value:_ 'CC' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ClientCenter' |
| ID | ID value. Stored as 'ID'. <br /> _Database Value:_ 'ID' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'ID' |
| ECommerce | ECommerce value. Stored as 'EC'. <br /> _Database Value:_ 'EC' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'ECommerce' |
| LEGALBG | LEGALBG value. Stored as 'LEG'. <br /> _Database Value:_ 'LEG' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'LEGALBG' |
| SocialInteractions | SocialInteractions value. Stored as 'SI'. <br /> _Database Value:_ 'SI' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'SocialInteractions' |
| DigitalMarketplace | DigitalMarketplace value. Stored as 'DM'. <br /> _Database Value:_ 'DM' <br /> _Model Value:_ 6 <br /> _Domain API Value:_ 'DigitalMarketplace' |
| UserProfile | UserProfile value. Stored as 'PFL'. <br /> _Database Value:_ 'PFL' <br /> _Model Value:_ 7 <br /> _Domain API Value:_ 'UserProfile' |
| WebClientApplication | WebClientApplication value. Stored as 'APP'. <br /> _Database Value:_ 'APP' <br /> _Model Value:_ 8 <br /> _Domain API Value:_ 'WebClientApplication' |
| TableAPI | TableAPI value. Stored as 'TAP'. <br /> _Database Value:_ 'TAP' <br /> _Model Value:_ 9 <br /> _Domain API Value:_ 'TableAPI' |
| DataAccessAPI | DataAccessAPI value. Stored as 'DAP'. <br /> _Database Value:_ 'DAP' <br /> _Model Value:_ 10 <br /> _Domain API Value:_ 'DataAccessAPI' |
| WMSMobileApp | ERP.net WMS Mobile App. Stored as 'WMS'. <br /> _Database Value:_ 'WMS' <br /> _Model Value:_ 11 <br /> _Domain API Value:_ 'WMSMobileApp' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company, for which is the site. null means, that the web site should not be enterprise company specific. [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TrustedApplication

> The trusted application related to this web site. [Filter(multi eq)] (Introduced in version 20.1.100.0)

_Type_: **[Systems.Security.TrustedApplications](Systems.Security.TrustedApplications.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### WebHost

> The web host in which to host the site. [Filter(multi eq)]

_Type_: **[Systems.Core.WebHosts](Systems.Core.WebHosts.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.WebSites erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.WebSites erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.WebSites erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_WebSites?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_WebSites?$top=10>

