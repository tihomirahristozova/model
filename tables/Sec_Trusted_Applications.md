# Table Sec_Trusted_Applications

Application, which is trusted to access the ERP data. Entity: Sec_Trusted_Applications (Introduced in version 19.1)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Trusted_Application_Id|`Guid`|`PK`, Readonly||
|Application_Secret_Hash|`String`||Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider. `Introduced in version 20.1` |
|Application_Uri|`String`||Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app". `Required` `Filter(eq)` |
|Basic_Authentication_Allowed|`Boolean`||Even if only one application has this turned ON, it allows the basic authentication for the whole database. Use with caution! If a user is specified in System User, the basic authentication is allowed only for this user. `Required` `Default(false)` `Filter(eq)` |
|Client_Type|`ClientType`|Allowed: `C`, `P`|Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app). `Required` `Default("C")` `Introduced in version 20.1` |
|Creation_Time_Utc|`DateTime`||Date and time (in UTC) when the application was registered. `Required` `Default(NowUtc)` `Filter(eq;ge;le)` |
|Impersonate_As_Community_User_Allowed|`Boolean`||Allows the application to request login from external users and operate on their behalf. `Required` `Default(false)` `Filter(eq)` |
|Impersonate_As_Internal_User_Allowed|`Boolean`||Allows the application to request login from internal users and operate on their behalf. `Required` `Default(false)` `Filter(eq)` |
|Impersonate_Login_Url|`String`||The login Url used when an application is impersonated as (usually community) user. |
|Impersonate_Logout_Url|`String`||The logout Url used when an application is impersonated as (usually community) user. |
|Is_Enabled|`Boolean`||Specifies whether the application is enabled for login. `Required` `Default(true)` `Filter(eq)` |
|Trusted_Application_Name|`String`||The multi-language name of the application. `Required` `Filter(eq;like)` |
|Notes|`String`||Notes for this TrustedApplication. |
|Scope|`String`||The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values). `Introduced in version 20.1` |
|System_User_Allowed|`Boolean`||Allows this application to logon as a service. `Required` `Default(false)` `Filter(eq)` |
|System_User_Login_Url|`String`||The URL, which will be used by the login process, when the application logs in as a service. |
