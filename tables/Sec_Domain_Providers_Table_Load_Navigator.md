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


Domain_Provider_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|yes|
|Order in Primary Key|1|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|NewGuid|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Domain_Provider_Id](Sec_Domain_Providers.md#domain_provider_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|0|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Domain_Id


Domain_Id


The domain for which the provider is setup.


The domain for which the provider is setup.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Domains](Sec_Domains.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Domain_Id](Sec_Domain_Providers.md#domain_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Provider_Name


Provider_Name


The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc.


The system name of the user authentication provider. For example GOOGLE, FACEBOOK, MICROSOFT, AZUREAD, ERPNET, etc.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`ERPNET`, `AZUREAD`, `GOOGLE`, `FACEBOOK`|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Provider_Name](Sec_Domain_Providers.md#provider_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Notes](Sec_Domain_Providers.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|3|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Row_Version


Row_Version

| Property | Value |
| - | - |
|Type|timestamp|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Row_Version](Sec_Domain_Providers.md#row_version)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|no|
|Max Length|-1|
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Active


Is_Active


Specifies whether the provider is currently active for the domain.


Specifies whether the provider is currently active for the domain.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|True|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Is_Active](Sec_Domain_Providers.md#is_active)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|5|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Client_ID


Client_ID


This is the Client_ID of our registration within the provider.


This is the Client_ID of our registration within the provider.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Client_ID](Sec_Domain_Providers.md#client_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|6|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Client_Secret


Client_Secret


This is the password, which we, as a client app, use to access the authentication provider.


This is the password, which we, as a client app, use to access the authentication provider.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Client_Secret](Sec_Domain_Providers.md#client_secret)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|7|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Tenant_ID


Tenant_ID


When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant.


When the authentication provider is multi-tenant, this specifies the tenant ID. For example, Google, Facebook and Microsoft are singe-tenant, while AzureAD is multi-tenant.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Tenant_ID](Sec_Domain_Providers.md#tenant_id)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|8|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Display_Name


Display_Name


Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers.


Specifies the (multi-language) display name of the button in the login form. Especially useful for multi-tenant providers.

| Property | Value |
| - | - |
|Type|nvarchar|
|Is Mulitlanguage|yes|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Domain_Providers](Sec_Domain_Providers.md).[Display_Name](Sec_Domain_Providers.md#display_name)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|yes|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|9|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


