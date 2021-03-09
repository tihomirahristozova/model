# Table Sec_Domain_Providers

The external authentication providers, linked to the domain. Contains data about registration, usually the app id or app key. Entity: Sec_Domain_Providers (Introduced in version 20.1)

## Owner Tables Hierarchy

* [Sec_Domains](Sec_Domains.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Domain_Provider_Id](#domain_provider_id)|`uniqueidentifier` `PK`||
|[Domain_Id](#domain_id)|`uniqueidentifier` |The domain for which the provider is setup.|
|[Provider_Name](#provider_name)|`nvarchar(256)` Allowed: `ERPNET`, `AZUREAD`, `GOOGLE`, `FACEBOOK`|The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the provider is currently active for the domain.|
|[Client_ID](#client_id)|`nvarchar(254)` |This is the Client_ID of our registration within the provider.|
|[Client_Secret](#client_secret)|`nvarchar(254)` |This is the password, which we, as a client app, use to access the authentication provider.|
|[Tenant_ID](#tenant_id)|`nvarchar(254)` |When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant.|
|[Display_Name](#display_name)|`nvarchar(254)` `ML`|Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers.|

## Columns

### Domain_Provider_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Domain_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Provider_Name

| Property | Value |
| - | - |
|Type|nvarchar(256)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Is_Active

| Property | Value |
| - | - |
|Type|bit|

### Client_ID

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Client_Secret

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Tenant_ID

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Display_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|


