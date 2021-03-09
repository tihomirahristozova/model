# Query Sec_Trusted_Applications_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Trusted_Application_Id](#trusted_application_id)|`uniqueidentifier` `PK`||
|[Trusted_Application_Name](#trusted_application_name)|`nvarchar` |The multi-language name of the application.|
|[Application_Uri](#application_uri)|`nvarchar` |Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app".|
|[Is_Enabled](#is_enabled)|`bit` |Specifies whether the application is enabled for login.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |Date and time (in UTC) when the application was registered.|
|[System_User_Allowed](#system_user_allowed)|`bit` |Specifies whether the application is allowed to securely obtain system user.|
|[System_User_Login_Url](#system_user_login_url)|`nvarchar` |When System User Allowed = true, specifies the login Url used by the function to securely obtain the system user.|
|[System_User_Id](#system_user_id)|`uniqueidentifier` |The user, which will be provided to the application if it requests system user.|
|[Impersonate_As_Community_User_Allowed](#impersonate_as_community_user_allowed)|`bit` |Specifies whether the application is allowed to impersonate itself as community user of the specified Community.|
|[Impersonate_As_Internal_User_Allowed](#impersonate_as_internal_user_allowed)|`bit` |Specifies whether the application is allowed to impersonate itself as internal user.|
|[Impersonate_Login_Url](#impersonate_login_url)|`nvarchar` |The login Url used when an application is impersonated as (usually community) user.|
|[Impersonate_Logout_Url](#impersonate_logout_url)|`nvarchar` |The logout Url used when an application is impersonated as (usually community) user.|
|[Basic_Authentication_Allowed](#basic_authentication_allowed)|`bit` |Specifies whether the application is allowed to use basic authentication for login. This is used to recognize applications, using basic authentication (when they use the same system user).|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||
|[Client_Type](#client_type)|`nvarchar` Allowed: `C`, `P`|Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app).|
|[Scope](#scope)|`nvarchar` |The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values).|
|[Application_Secret_Hash](#application_secret_hash)|`nvarchar` |Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider.|

## Columns

### Trusted_Application_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Trusted_Application_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Application_Uri

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

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
|Type|nvarchar|

### Impersonate_Logout_Url

| Property | Value |
| - | - |
|Type|nvarchar|

### Basic_Authentication_Allowed

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Client_Type

| Property | Value |
| - | - |
|Type|nvarchar|

### Scope

| Property | Value |
| - | - |
|Type|nvarchar|

### Application_Secret_Hash

| Property | Value |
| - | - |
|Type|nvarchar|


