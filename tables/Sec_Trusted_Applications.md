# Table Sec_Trusted_Applications

Application, which is trusted to access the ERP data. Entity: Sec_Trusted_Applications (Introduced in version 19.1)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Trusted_Application_Id](#trusted_application_id)|`uniqueidentifier` `PK`||
|[Trusted_Application_Name](#trusted_application_name)|`nvarchar(254)` |The multi-language name of the application.|
|[Application_Uri](#application_uri)|`nvarchar(254)` |Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app".|
|[Is_Enabled](#is_enabled)|`bit` |Specifies whether the application is enabled for login.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |Date and time (in UTC) when the application was registered.|
|[System_User_Allowed](#system_user_allowed)|`bit` |Allows this application to logon as a service.|
|[System_User_Login_Url](#system_user_login_url)|`nvarchar(254)` |The URL, which will be used by the login process, when the application logs in as a service.|
|[System_User_Id](#system_user_id)|`uniqueidentifier` |The user, which will be used when the application logins as a service.|
|[Impersonate_As_Community_User_Allowed](#impersonate_as_community_user_allowed)|`bit` |Allows the application to request login from external users and operate on their behalf.|
|[Impersonate_As_Internal_User_Allowed](#impersonate_as_internal_user_allowed)|`bit` |Allows the application to request login from internal users and operate on their behalf.|
|[Impersonate_Login_Url](#impersonate_login_url)|`nvarchar(254)` |The login Url used when an application is impersonated as (usually community) user.|
|[Impersonate_Logout_Url](#impersonate_logout_url)|`nvarchar(254)` |The logout Url used when an application is impersonated as (usually community) user.|
|[Basic_Authentication_Allowed](#basic_authentication_allowed)|`bit` |Even if only one application has this turned ON, it allows the basic authentication for the whole database. Use with caution! If a user is specified in System User, the basic authentication is allowed only for this user.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Client_Type](#client_type)|`nvarchar(1)` Allowed: `C`, `P`|Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app).|
|[Scope](#scope)|`nvarchar(2147483647)` |The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values).|
|[Application_Secret_Hash](#application_secret_hash)|`nvarchar(250)` |Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider.|

## Columns

### Trusted_Application_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Trusted_Application_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Application_Uri

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Is_Enabled

| Property | Value |
| - | - |
|Type|bit|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### System_User_Allowed

| Property | Value |
| - | - |
|Type|bit|

### System_User_Login_Url

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### System_User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Impersonate_As_Community_User_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Impersonate_As_Internal_User_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Impersonate_Login_Url

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Impersonate_Logout_Url

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Basic_Authentication_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Client_Type

| Property | Value |
| - | - |
|Type|nvarchar(1)|

### Scope

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Application_Secret_Hash

| Property | Value |
| - | - |
|Type|nvarchar(250)|


