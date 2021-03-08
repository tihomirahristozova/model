# Table Sec_Domain_Providers

The external authentication providers, linked to the domain. Contains data about registration, usually the app id or app key. Entity: Sec_Domain_Providers (Introduced in version 20.1)

# Aggregate Hierarchy

* [Sec_Domains](Sec_Domains.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Domain_Provider_Id|`Guid`|`PK`, Readonly||
|Client_ID|`String`||This is the Client_ID of our registration within the provider. |
|Client_Secret|`String`||This is the password, which we, as a client app, use to access the authentication provider. |
|Display_Name|`MultilanguageString`||Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers. |
|Is_Active|`Boolean`||Specifies whether the provider is currently active for the domain. `Required` `Default(true)` `Filter(eq)` |
|Notes|`String`||Notes for this DomainProvider. |
|Provider_Name|`ProviderName`|Allowed: `ERPNET`, `AZUREAD`, `GOOGLE`, `FACEBOOK`|The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc. `Required` `Filter(eq)` |
|Tenant_ID|`String`||When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant. |
