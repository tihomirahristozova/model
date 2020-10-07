# Systems.Security.UserProviderLogins

External login providers. Entity: Sec_User_Provider_Logins (Introduced in version 18.2.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.UserProviderLogins.md#Id) | guid |  
| [ProviderKey](Systems.Security.UserProviderLogins.md#ProviderKey) | string | The key, which the provider provided for logging the user. [Required] [Filter(multi eq)] 
| [ProviderName](Systems.Security.UserProviderLogins.md#ProviderName) | [Systems.Security.DomainProvidersRepository.ProviderName](Systems.Security.UserProviderLogins.md#ProviderName) | The system name of the authentication provider. It should be already registered for the domain. [Required] [Filter(eq)] (Introduced in version 20.1.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [User](Systems.Security.UserProviderLogins.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The user for which the login is defined. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ProviderKey

> The key, which the provider provided for logging the user. [Required] [Filter(multi eq)]

_Type_: **string**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ProviderName

> The system name of the authentication provider. It should be already registered for the domain. [Required] [Filter(eq)] (Introduced in version 20.1.100.0)

_Type_: **[Systems.Security.DomainProvidersRepository.ProviderName](Systems.Security.UserProviderLogins.md#ProviderName)**  
Allowed values for the [ProviderName](Systems.Security.DomainProviders.md#ProviderName) data attribute  
_Allowed Values (Enum Members)_  

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

> The user for which the login is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.UserProviderLogins erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.UserProviderLogins erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.UserProviderLogins erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_UserProviderLogins?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_UserProviderLogins?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_User_Provider_Logins?$top=10>

