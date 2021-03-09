# Query Sec_Domain_Providers_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Domain_Provider_Id](#domain_provider_id)|`uniqueidentifier` `PK`||
|[Domain_Id](#domain_id)|`uniqueidentifier` |The domain for which the provider is setup.|
|[Provider_Name](#provider_name)|`nvarchar` Allowed: `ERPNET`, `AZUREAD`, `GOOGLE`, `FACEBOOK`|The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Is_Active](#is_active)|`bit` |Specifies whether the provider is currently active for the domain.|
|[Client_ID](#client_id)|`nvarchar` |This is the Client_ID of our registration within the provider.|
|[Client_Secret](#client_secret)|`nvarchar` |This is the password, which we, as a client app, use to access the authentication provider.|
|[Tenant_ID](#tenant_id)|`nvarchar` |When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant.|
|[Display_Name](#display_name)|`nvarchar` `ML`|Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers.|

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
|Type|nvarchar|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Client_Secret

| Property | Value |
| - | - |
|Type|nvarchar|

### Tenant_ID

| Property | Value |
| - | - |
|Type|nvarchar|

### Display_Name

| Property | Value |
| - | - |
|Type|nvarchar|


