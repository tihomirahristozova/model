---
uid: Systems.Security.UserProviderLogins
---
# Systems.Security.UserProviderLogins Entity

External login providers. Entity: Sec_User_Provider_Logins (Introduced in version 18.2)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.UserProviderLogins.md#id) | guid |  
| [ProviderKey](Systems.Security.UserProviderLogins.md#providerkey) | string | The key, which the provider provided for logging the user. [Required] [Filter(multi eq)] 
| [ProviderName](Systems.Security.UserProviderLogins.md#providername) | [ProviderName](Systems.Security.UserProviderLogins.md#providername) | The system name of the authentication provider. It should be already registered for the domain. [Required] [Filter(eq)] (Introduced in version 20.1) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [User](Systems.Security.UserProviderLogins.md#user) | [Users](Systems.Security.Users.md) | The user for which the login is defined. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ProviderKey

The key, which the provider provided for logging the user. [Required] [Filter(multi eq)]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProviderName

The system name of the authentication provider. It should be already registered for the domain. [Required] [Filter(eq)] (Introduced in version 20.1)

_Type_: **[ProviderName](Systems.Security.UserProviderLogins.md#providername)**  
Allowed values for the [ProviderName](Systems.Security.DomainProviders.md#providername) data attribute  
_Allowed Values (Systems.Security.DomainProvidersRepository.ProviderName Enum Members)_  

| Value | Description |
| ---- | --- |
| ERPNET | ERPNET value. Stored as 'ERPNET'. <br /> _Database Value:_ 'ERPNET' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ERPNET' |
| AZUREAD | AZUREAD value. Stored as 'AZUREAD'. <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AZUREAD' |
| GOOGLE | GOOGLE value. Stored as 'GOOGLE'. <br /> _Database Value:_ 'GOOGLE' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'GOOGLE' |
| FACEBOOK | FACEBOOK value. Stored as 'FACEBOOK'. <br /> _Database Value:_ 'FACEBOOK' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FACEBOOK' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  


## Reference Details

### User

The user for which the login is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Security.UserProviderLogins erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.UserProviderLogins erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_UserProviderLogins?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_UserProviderLogins?$top=10>

