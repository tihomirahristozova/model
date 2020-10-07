# Systems.Security.TrustedApplicationAuthorizations

Authorization of a trusted application to access the data on behalf of a context user. Entity: Sec_Trusted_Application_Authorizations (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.TrustedApplicationAuthorizations.md#Id) | guid |  
| [GrantTimeUtc](Systems.Security.TrustedApplicationAuthorizations.md#GrantTimeUtc) | datetime | The time (in UTC) when the authorization was granted. [Required] [Default(NowUtc)] 
| [IsRevoked](Systems.Security.TrustedApplicationAuthorizations.md#IsRevoked) | boolean | Specifies whether the grant is explicitly revoked. [Required] [Default(false)] 
| [Notes](Systems.Security.TrustedApplicationAuthorizations.md#Notes) | string (nullable) | Notes for this TrustedApplicationAuthorization. 
| [ValidFromUtc](Systems.Security.TrustedApplicationAuthorizations.md#ValidFromUtc) | datetime (nullable) | The start of the validitiy of the authorization. null means that there is no restriction. 
| [ValidUntilUtc](Systems.Security.TrustedApplicationAuthorizations.md#ValidUntilUtc) | datetime (nullable) | The time (in UTC) when the grant expires. null means that there is no time restriction. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContextUser](Systems.Security.TrustedApplicationAuthorizations.md#ContextUser) | [Systems.Security.Users](Systems.Security.Users.md) | The user, whose permissions are granted to the application. [Required] [Filter(multi eq)] |
| [GrantingUser](Systems.Security.TrustedApplicationAuthorizations.md#GrantingUser) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who authorized the application. [Required] [Filter(multi eq)] |
| [TrustedApplication](Systems.Security.TrustedApplicationAuthorizations.md#TrustedApplication) | [Systems.Security.TrustedApplications](Systems.Security.TrustedApplications.md) | The application, which is authorized. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### GrantTimeUtc

> The time (in UTC) when the authorization was granted. [Required] [Default(NowUtc)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### IsRevoked

> Specifies whether the grant is explicitly revoked. [Required] [Default(false)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

> Notes for this TrustedApplicationAuthorization.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidFromUtc

> The start of the validitiy of the authorization. null means that there is no restriction.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidUntilUtc

> The time (in UTC) when the grant expires. null means that there is no time restriction.

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ContextUser

> The user, whose permissions are granted to the application. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### GrantingUser

> The user, who authorized the application. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TrustedApplication

> The application, which is authorized. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Security.TrustedApplications](Systems.Security.TrustedApplications.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.TrustedApplicationAuthorizations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.TrustedApplicationAuthorizations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.TrustedApplicationAuthorizations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_TrustedApplicationAuthorizations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_TrustedApplicationAuthorizations?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_Trusted_Application_Authorizations?$top=10>

