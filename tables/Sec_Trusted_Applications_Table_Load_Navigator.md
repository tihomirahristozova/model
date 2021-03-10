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


Trusted_Application_Id

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Trusted_Application_Id](Sec_Trusted_Applications.md#trusted_application_id)|
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

### Trusted_Application_Name


Trusted_Application_Name


The multi-language name of the application.


The multi-language name of the application.

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
|Default Value|None|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Trusted_Application_Name](Sec_Trusted_Applications.md#trusted_application_name)|
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
|Order|1|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### Application_Uri


Application_Uri


Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app".


Application globally unique Uri in reverse host name format. For example: "com.manufacturer/app".

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
|Default Value|None|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Application_Uri](Sec_Trusted_Applications.md#application_uri)|
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

### Is_Enabled


Is_Enabled


Specifies whether the application is enabled for login.


Specifies whether the application is enabled for login.

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Is_Enabled](Sec_Trusted_Applications.md#is_enabled)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Creation_Time_Utc


Creation_Time_Utc


Date and time (in UTC) when the application was registered.


Date and time (in UTC) when the application was registered.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTimeUtc|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Creation_Time_Utc](Sec_Trusted_Applications.md#creation_time_utc)|
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
|Order|4|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### System_User_Allowed


System_User_Allowed


Specifies whether the application is allowed to securely obtain system user.


Specifies whether the application is allowed to securely obtain system user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[System_User_Allowed](Sec_Trusted_Applications.md#system_user_allowed)|
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

### System_User_Login_Url


System_User_Login_Url


When System User Allowed = true, specifies the login Url used by the function to securely obtain the system user.


When System User Allowed = true, specifies the login Url used by the function to securely obtain the system user.

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[System_User_Login_Url](Sec_Trusted_Applications.md#system_user_login_url)|
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

### System_User_Id


System_User_Id


The user, which will be provided to the application if it requests system user.


The user, which will be provided to the application if it requests system user.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[System_User_Id](Sec_Trusted_Applications.md#system_user_id)|
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
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Impersonate_As_Community_User_Allowed


Impersonate_As_Community_User_Allowed


Specifies whether the application is allowed to impersonate itself as community user of the specified Community.


Specifies whether the application is allowed to impersonate itself as community user of the specified Community.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Impersonate_As_Community_User_Allowed](Sec_Trusted_Applications.md#impersonate_as_community_user_allowed)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Impersonate_As_Internal_User_Allowed


Impersonate_As_Internal_User_Allowed


Specifies whether the application is allowed to impersonate itself as internal user.


Specifies whether the application is allowed to impersonate itself as internal user.

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Impersonate_As_Internal_User_Allowed](Sec_Trusted_Applications.md#impersonate_as_internal_user_allowed)|
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

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Impersonate_Login_Url


Impersonate_Login_Url


The login Url used when an application is impersonated as (usually community) user.


The login Url used when an application is impersonated as (usually community) user.

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Impersonate_Login_Url](Sec_Trusted_Applications.md#impersonate_login_url)|
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
|Order|10|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Impersonate_Logout_Url


Impersonate_Logout_Url


The logout Url used when an application is impersonated as (usually community) user.


The logout Url used when an application is impersonated as (usually community) user.

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Impersonate_Logout_Url](Sec_Trusted_Applications.md#impersonate_logout_url)|
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
|Order|11|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Basic_Authentication_Allowed


Basic_Authentication_Allowed


Specifies whether the application is allowed to use basic authentication for login. This is used to recognize applications, using basic authentication (when they use the same system user).


Specifies whether the application is allowed to use basic authentication for login. This is used to recognize applications, using basic authentication (when they use the same system user).

| Property | Value |
| - | - |
|Type|bit|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|False|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Basic_Authentication_Allowed](Sec_Trusted_Applications.md#basic_authentication_allowed)|
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
|Order|12|
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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Notes](Sec_Trusted_Applications.md#notes)|
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
|Order|13|
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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Row_Version](Sec_Trusted_Applications.md#row_version)|
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
|Order|14|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Client_Type


Client_Type


Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app).


Specifies the client type, according to RFC 6749, e.g. the confidentiality of the client app. P=Public (e.g. browser or native app); C=Confidential (e.g. web server app).

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
|Allowed Values|`C`, `P`|
|Default Value|C|
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Client_Type](Sec_Trusted_Applications.md#client_type)|
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
|Order|15|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Scope


Scope


The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values).


The scope (according to RFC 6749) for which the application was trusted. The scope is an unordered list of space-delimited case-sensitive strings. Each string denotes a permission (see docs for possible values).

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Scope](Sec_Trusted_Applications.md#scope)|
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
|Order|16|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Application_Secret_Hash


Application_Secret_Hash


Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider.


Hash of the secret of the client application. The secret is used when the client application needs to authorize itself in front of the identity provider.

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
|Derived From|[Sec_Trusted_Applications](Sec_Trusted_Applications.md).[Application_Secret_Hash](Sec_Trusted_Applications.md#application_secret_hash)|
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
|Order|17|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


