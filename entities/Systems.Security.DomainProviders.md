---
uid: Systems.Security.DomainProviders
---
# Systems.Security.DomainProviders Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

The external authentication providers, linked to the domain. Contains data about registration, usually the app id or app key. Entity: Sec_Domain_Providers (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{DisplayName:T}_  
Default Search Member:  
_DisplayName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Security.Domains](Systems.Security.Domains.md)  
Aggregate Root:  
[Systems.Security.Domains](Systems.Security.Domains.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ClientID](Systems.Security.DomainProviders.md#clientid) | string (254) __nullable__ | This is the Client_ID of our registration within the provider. 
| [ClientSecret](Systems.Security.DomainProviders.md#clientsecret) | string (254) __nullable__ | This is the password, which we, as a client app, use to access the authentication provider. 
| [DisplayName](Systems.Security.DomainProviders.md#displayname) | [MultilanguageString](../data-types.md#multilanguagestring) __nullable__ | Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers. 
| [Id](Systems.Security.DomainProviders.md#id) | guid |  
| [IsActive](Systems.Security.DomainProviders.md#isactive) | boolean | Specifies whether the provider is currently active for the domain. `Required` `Default(true)` `Filter(eq)` 
| [Notes](Systems.Security.DomainProviders.md#notes) | string (max) __nullable__ | Notes for this DomainProvider. 
| [ProviderName](Systems.Security.DomainProviders.md#providername) | [ProviderName](Systems.Security.DomainProviders.md#providername) | The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc. `Required` `Filter(eq)` 
| [TenantID](Systems.Security.DomainProviders.md#tenantid) | string (254) __nullable__ | When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Domain](Systems.Security.DomainProviders.md#domain) | [Domains](Systems.Security.Domains.md) | The domain for which the provider is setup. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ClientID

This is the Client_ID of our registration within the provider.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ClientSecret

This is the password, which we, as a client app, use to access the authentication provider.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### DisplayName

Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers.

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the provider is currently active for the domain. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for this DomainProvider.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ProviderName

The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc. `Required` `Filter(eq)`

_Type_: **[ProviderName](Systems.Security.DomainProviders.md#providername)**  
Allowed values for the `ProviderName`(Systems.Security.DomainProviders.md#providername) data attribute  
_Allowed Values (Systems.Security.DomainProvidersRepository.ProviderName Enum Members)_  

| Value | Description |
| ---- | --- |
| ERPNET | ERPNET value. Stored as 'ERPNET'. <br /> _Database Value:_ 'ERPNET' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ERPNET' |
| AZUREAD | AZUREAD value. Stored as 'AZUREAD'. <br /> _Database Value:_ 'AZUREAD' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AZUREAD' |
| GOOGLE | GOOGLE value. Stored as 'GOOGLE'. <br /> _Database Value:_ 'GOOGLE' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'GOOGLE' |
| FACEBOOK | FACEBOOK value. Stored as 'FACEBOOK'. <br /> _Database Value:_ 'FACEBOOK' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FACEBOOK' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### TenantID

When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### Domain

The domain for which the provider is setup. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Domains](Systems.Security.Domains.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Security.DomainProviders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.DomainProviders erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_DomainProviders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_DomainProviders?$top=10>

