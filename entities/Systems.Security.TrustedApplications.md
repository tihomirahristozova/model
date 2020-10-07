# Systems.Security.TrustedApplications

Application, which is trusted to access the ERP data. Entity: Sec_Trusted_Applications (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.TrustedApplications.md#Id) | guid |  
| [ApplicationSecretHash](Systems.Security.TrustedApplications.md#ApplicationSecretHash) | string (nullable) | Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider. (Introduced in version 20.1.100.0) 
| [ApplicationUri](Systems.Security.TrustedApplications.md#ApplicationUri) | string | Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app". [Required] [Filter(eq)] 
| [BasicAuthenticationAllowed](Systems.Security.TrustedApplications.md#BasicAuthenticationAllowed) | boolean | Even if only one application has this turned ON, it allows the basic authentication for the whole database. Use with caution! If a user is specified in System User, the basic authentication is allowed only for this user. [Required] [Default(false)] [Filter(eq)] 
| [ClientType](Systems.Security.TrustedApplications.md#ClientType) | [Systems.Security.TrustedApplicationsRepository.ClientType](Systems.Security.TrustedApplications.md#ClientType) | Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app). [Required] [Default("C")] (Introduced in version 20.1.100.0) 
| [CreationTimeUtc](Systems.Security.TrustedApplications.md#CreationTimeUtc) | datetime | Date and time (in UTC) when the application was registered. [Required] [Default(NowUtc)] [Filter(eq;ge;le)] 
| [ImpersonateAsCommunityUserAllowed](Systems.Security.TrustedApplications.md#ImpersonateAsCommunityUserAllowed) | boolean | Allows the application to request login from external users and operate on their behalf. [Required] [Default(false)] [Filter(eq)] 
| [ImpersonateAsInternalUserAllowed](Systems.Security.TrustedApplications.md#ImpersonateAsInternalUserAllowed) | boolean | Allows the application to request login from internal users and operate on their behalf. [Required] [Default(false)] [Filter(eq)] 
| [ImpersonateLoginUrl](Systems.Security.TrustedApplications.md#ImpersonateLoginUrl) | string (nullable) | The login Url used when an application is impersonated as (usually community) user. 
| [ImpersonateLogoutUrl](Systems.Security.TrustedApplications.md#ImpersonateLogoutUrl) | string (nullable) | The logout Url used when an application is impersonated as (usually community) user. 
| [IsEnabled](Systems.Security.TrustedApplications.md#IsEnabled) | boolean | Specifies whether the application is enabled for login. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Systems.Security.TrustedApplications.md#Notes) | string (nullable) | Notes for this TrustedApplication. 
| [Scope](Systems.Security.TrustedApplications.md#Scope) | string (nullable) | The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values). (Introduced in version 20.1.100.0) 
| [SystemUserAllowed](Systems.Security.TrustedApplications.md#SystemUserAllowed) | boolean | Allows this application to logon as a service. [Required] [Default(false)] [Filter(eq)] 
| [SystemUserLoginUrl](Systems.Security.TrustedApplications.md#SystemUserLoginUrl) | string (nullable) | The URL, which will be used by the login process, when the application logs in as a service. 
| [Name](Systems.Security.TrustedApplications.md#Name) | string | The multi-language name of the application. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [SystemUser](Systems.Security.TrustedApplications.md#SystemUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user, which will be used when the application logins as a service. [Filter(multi eq)] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Authorizations | [Systems.Security.TrustedApplicationAuthorizations](Systems.Security.TrustedApplicationAuthorizations.md) | List of [TrustedApplicationAuthorization](Systems.Security.TrustedApplicationAuthorizations.md) child objects, based on the [Systems.Security.TrustedApplicationAuthorization.TrustedApplication](Systems.Security.TrustedApplicationAuthorizations.md#TrustedApplication) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ApplicationSecretHash

> Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider. (Introduced in version 20.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ApplicationUri

> Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app". [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### BasicAuthenticationAllowed

> Even if only one application has this turned ON, it allows the basic authentication for the whole database. Use with caution! If a user is specified in System User, the basic authentication is allowed only for this user. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ClientType

> Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app). [Required] [Default("C")] (Introduced in version 20.1.100.0)

_Type_: **[Systems.Security.TrustedApplicationsRepository.ClientType](Systems.Security.TrustedApplications.md#ClientType)**  
Allowed values for the [ClientType](Systems.Security.TrustedApplications.md#ClientType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Confidential | Confidential value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Confidential' |
| Public | Public value. Stored as 'P'. <br /> _Database Value:_ 'P' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Public' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **Confidential**  

### CreationTimeUtc

> Date and time (in UTC) when the application was registered. [Required] [Default(NowUtc)] [Filter(eq;ge;le)]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### ImpersonateAsCommunityUserAllowed

> Allows the application to request login from external users and operate on their behalf. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ImpersonateAsInternalUserAllowed

> Allows the application to request login from internal users and operate on their behalf. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ImpersonateLoginUrl

> The login Url used when an application is impersonated as (usually community) user.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ImpersonateLogoutUrl

> The logout Url used when an application is impersonated as (usually community) user.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsEnabled

> Specifies whether the application is enabled for login. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this TrustedApplication.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Scope

> The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values). (Introduced in version 20.1.100.0)

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### SystemUserAllowed

> Allows this application to logon as a service. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### SystemUserLoginUrl

> The URL, which will be used by the login process, when the application logs in as a service.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The multi-language name of the application. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### SystemUser

> The user, which will be used when the application logins as a service. [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.TrustedApplications erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.TrustedApplications erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.TrustedApplications erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_TrustedApplications?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_TrustedApplications?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_Trusted_Applications?$top=10>

