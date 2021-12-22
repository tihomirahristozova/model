---
uid: Systems.Security.TrustedApplicationAuthorizations
---
# Systems.Security.TrustedApplicationAuthorizations Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Authorization of a trusted application to access the data on behalf of a context user. Entity: Sec_Trusted_Application_Authorizations (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{TrustedApplication.Name}_  
Default Search Members:  
_TrustedApplication.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Security.TrustedApplications](Systems.Security.TrustedApplications.md)  
Aggregate Root:  
[Systems.Security.TrustedApplications](Systems.Security.TrustedApplications.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [GrantTimeUtc](Systems.Security.TrustedApplicationAuthorizations.md#granttimeutc) | datetime | The time (in UTC) when the authorization was granted. `Required` `Default(NowUtc)` 
| [Id](Systems.Security.TrustedApplicationAuthorizations.md#id) | guid |  
| [IsRevoked](Systems.Security.TrustedApplicationAuthorizations.md#isrevoked) | boolean | Specifies whether the grant is explicitly revoked. `Required` `Default(false)` 
| [Notes](Systems.Security.TrustedApplicationAuthorizations.md#notes) | string (max) __nullable__ | Notes for this TrustedApplication<br />Authorization. 
| [ObjectVersion](Systems.Security.TrustedApplicationAuthorizations.md#objectversion) | int32 |  
| [ValidFromUtc](Systems.Security.TrustedApplicationAuthorizations.md#validfromutc) | datetime __nullable__ | The start of the validitiy of the authorization. null means that there is no restriction. 
| [ValidUntilUtc](Systems.Security.TrustedApplicationAuthorizations.md#validuntilutc) | datetime __nullable__ | The time (in UTC) when the grant expires. null means that there is no time restriction. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ContextUser](Systems.Security.TrustedApplicationAuthorizations.md#contextuser) | [Users](Systems.Security.Users.md) | The user, whose permissions are granted to the application. `Required` `Filter(multi eq)` |
| [GrantingUser](Systems.Security.TrustedApplicationAuthorizations.md#grantinguser) | [Users](Systems.Security.Users.md) | The user, who authorized the application. `Required` `Filter(multi eq)` |
| [TrustedApplication](Systems.Security.TrustedApplicationAuthorizations.md#trustedapplication) | [TrustedApplications](Systems.Security.TrustedApplications.md) | The application, which is authorized. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### GrantTimeUtc

The time (in UTC) when the authorization was granted. `Required` `Default(NowUtc)`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsRevoked

Specifies whether the grant is explicitly revoked. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

Notes for this TrustedApplicationAuthorization.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ValidFromUtc

The start of the validitiy of the authorization. null means that there is no restriction.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ValidUntilUtc

The time (in UTC) when the grant expires. null means that there is no time restriction.

_Type_: **datetime __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ContextUser

The user, whose permissions are granted to the application. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### GrantingUser

The user, who authorized the application. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### TrustedApplication

The application, which is authorized. `Required` `Filter(multi eq)` `Owner`

_Type_: **[TrustedApplications](Systems.Security.TrustedApplications.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Security.TrustedApplicationAuthorizations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.TrustedApplicationAuthorizations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_TrustedApplicationAuthorizations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_TrustedApplicationAuthorizations?$top=10>

