# Systems.Security.DomainProviders

The external authentication providers, linked to the domain. Contains data about registration, usually the app id or app key. Entity: Sec_Domain_Providers (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.DomainProviders.md#Id) | guid |  
| [ClientID](Systems.Security.DomainProviders.md#ClientID) | string (nullable) | This is the Client_ID of our registration within the provider. 
| [ClientSecret](Systems.Security.DomainProviders.md#ClientSecret) | string (nullable) | This is the password, which we, as a client app, use to access the authentication provider. 
| [DisplayName](Systems.Security.DomainProviders.md#DisplayName) | [MultilanguageString](../data-types/MultilanguageString.md) (nullable) | Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers. 
| [IsActive](Systems.Security.DomainProviders.md#IsActive) | boolean | Specifies whether the provider is currently active for the domain. [Required] [Default(true)] [Filter(eq)] 
| [Notes](Systems.Security.DomainProviders.md#Notes) | string (nullable) | Notes for this DomainProvider. 
| [ProviderName](Systems.Security.DomainProviders.md#ProviderName) | [Systems.Security.DomainProvidersRepository.ProviderName](Systems.Security.DomainProviders.md#ProviderName) | The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc. [Required] [Filter(eq)] 
| [TenantID](Systems.Security.DomainProviders.md#TenantID) | string (nullable) | When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Domain](Systems.Security.DomainProviders.md#Domain) | [Systems.Security.Domains](Systems.Security.Domains.md) | The domain for which the provider is setup. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### ClientID

> This is the Client_ID of our registration within the provider.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ClientSecret

> This is the password, which we, as a client app, use to access the authentication provider.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DisplayName

> Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers.

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### IsActive

> Specifies whether the provider is currently active for the domain. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this DomainProvider.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ProviderName

> The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc. [Required] [Filter(eq)]

_Type_: **[Systems.Security.DomainProvidersRepository.ProviderName](Systems.Security.DomainProviders.md#ProviderName)**  
Allowed values for the [ProviderName](Systems.Security.DomainProviders.md#ProviderName) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| ERPNET | ERPNET value. Stored as 'ERPNET'. <br /> _Database Value:_ 'ERPNET' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'ERPNET' |
| AZUREAD | AZUREAD value. Stored as 'AZUREAD'. <br /> _Database Value:_ 'AZUREAD' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AZUREAD' |
| GOOGLE | GOOGLE value. Stored as 'GOOGLE'. <br /> _Database Value:_ 'GOOGLE' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'GOOGLE' |
| FACEBOOK | FACEBOOK value. Stored as 'FACEBOOK'. <br /> _Database Value:_ 'FACEBOOK' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'FACEBOOK' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### TenantID

> When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Domain

> The domain for which the provider is setup. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Systems.Security.Domains](Systems.Security.Domains.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.DomainProviders erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.DomainProviders erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.DomainProviders erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_DomainProviders?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_DomainProviders?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_Domain_Providers?$top=10>

