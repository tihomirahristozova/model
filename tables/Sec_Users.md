# Table Sec_Users

User logins. Entity: Sec_Users

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Id](#user_id)|`uniqueidentifier` `PK`||
|[Login](#login)|`nvarchar(64)` |The login name of the user, which is usually the email|
|[User_Name](#user_name)|`nvarchar(254)` `ML`|The full name of the user|
|[Password](#password)|`nvarchar(64)` |The password hash of the user, stored in the format, specified in Password Format.|
|[Is_Admin](#is_admin)|`bit` |1 if the user is administrator, otherwise 0.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Person_Id](#person_id)|`uniqueidentifier` |The person from within the system, which is authenticated with this login. NULL means that this user is not associated with a person record in the database.|
|[Active](#active)|`bit` |True when the login is currently active and the user can log in.|
|[Windows_User_Name](#windows_user_name)|`nvarchar(128)` |The Windows (Active Directory) user, to which this login is bound. The user will be allowed to login only when the client machine is logged in Active Directory with the specified user.|
|[Voice_Extension_Numbers](#voice_extension_numbers)|`nvarchar(254)` |Comma separated list of internal extension numbers of the voice telephones of the user. Used for VOIP integration|
|[Row_Version](#row_version)|`timestamp` ||
|[Access_Failed_Count](#access_failed_count)|`int` |Indicates how many times the user has failed to login. May be used for locking out the user.|
|[Email](#email)|`nvarchar(254)` |Unique email of the user. Can be NULL because there may be login providers that don't use emails.|
|[Email_Confirmed](#email_confirmed)|`bit` |Indicates whether the email address for the specified user has been verified.|
|[Lockout_End_Utc](#lockout_end_utc)|`datetime` |Contains the date and time (in UTC) until the user is locked. NULL when the user is not locked.|
|[Password_Format](#password_format)|`nvarchar(3)` Allowed: `MD5`, `AN3`|The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3.|
|[Phone_Number](#phone_number)|`nvarchar(64)` |Used only for two-factor authentication. NULL when phone-based two-factor is not used.|
|[Phone_Number_Confirmed](#phone_number_confirmed)|`bit` |Indicates whether the Phone Number has been verified.|
|[Two_Factor_Enabled](#two_factor_enabled)|`bit` |Indicates whether two-factor authentication has been enabled.|
|[User_Type](#user_type)|`nvarchar(3)` Allowed: `INT`, `EXT`, `VIR`, `SYS`, `APP`|Specifies the user type. INT=Internal; EXT=External (community); VIR=Virtual (No login); SYS=System; APP=Application.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` Readonly|The date and time (in UTC), when the user was created.|
|[Domain_Id](#domain_id)|`uniqueidentifier` |The domain, to which the user belongs.|
|[Default_Culture](#default_culture)|`nvarchar(15)` |The preferred default culture of the user for UI, notifications, etc. NULL means "en-US".|

## Columns

### User_Id


User_Id

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
|Derived From|[Sec_Users](Sec_Users.md).[User_Id](Sec_Users.md#user_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Login


Login


The login name of the user, which is usually the email


The login name of the user, which is usually the email

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Login](Sec_Users.md#login)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|Like|None|no|no|

### User_Name


User_Name


The full name of the user


The full name of the user

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|yes|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[User_Name](Sec_Users.md#user_name)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Like|None|no|no|

### Password


Password


The password hash of the user, stored in the format, specified in Password Format.


The password hash of the user, stored in the format, specified in Password Format.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Password](Sec_Users.md#password)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Is_Admin


Is_Admin


1 if the user is administrator, otherwise 0.


1 if the user is administrator, otherwise 0.

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
|Derived From|[Sec_Users](Sec_Users.md).[Is_Admin](Sec_Users.md#is_admin)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|-1|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Notes


Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None, IsLongString|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Notes](Sec_Users.md#notes)|
|Format||
|Ignore for Insert Order|no|
|Auto Complete|no|
|Data Filter|no|
|Enter Stop|no|
|Is Entity Name|no|
|Password|no|
|Is Picture|no|
|Is RTF|no|
|Is User Login|no|
|Visible|yes|
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Short|
|Supports EQUALS_IN|no|

### Person_Id


Person_Id


The person from within the system, which is authenticated with this login. NULL means that this user is not associated with a person record in the database.


The person from within the system, which is authenticated with this login. NULL means that this user is not associated with a person record in the database.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Cm_Persons](Cm_Persons.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Person_Id](Sec_Users.md#person_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|100|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Active


Active


True when the login is currently active and the user can log in.


True when the login is currently active and the user can log in.

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
|Derived From|[Sec_Users](Sec_Users.md).[Active](Sec_Users.md#active)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|yes|

### Windows_User_Name


Windows_User_Name


The Windows (Active Directory) user, to which this login is bound. The user will be allowed to login only when the client machine is logged in Active Directory with the specified user.


The Windows (Active Directory) user, to which this login is bound. The user will be allowed to login only when the client machine is logged in Active Directory with the specified user.

| Property | Value |
| - | - |
|Type|nvarchar(128)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Windows_User_Name](Sec_Users.md#windows_user_name)|
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
|Max Length|128|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Voice_Extension_Numbers


Voice_Extension_Numbers


Comma separated list of internal extension numbers of the voice telephones of the user. Used for VOIP integration


Comma separated list of internal extension numbers of the voice telephones of the user. Used for VOIP integration

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Voice_Extension_Numbers](Sec_Users.md#voice_extension_numbers)|
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
|Max Length|254|
|Order|2147483647|
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
|Derived From|[Sec_Users](Sec_Users.md).[Row_Version](Sec_Users.md#row_version)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Access_Failed_Count


Access_Failed_Count


Indicates how many times the user has failed to login. May be used for locking out the user.


Indicates how many times the user has failed to login. May be used for locking out the user.

| Property | Value |
| - | - |
|Type|int|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|0|
|Derived From|[Sec_Users](Sec_Users.md).[Access_Failed_Count](Sec_Users.md#access_failed_count)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|
|GreaterThanOrLessThan|None|no|no|

### Email


Email


Unique email of the user. Can be NULL because there may be login providers that don't use emails.


Unique email of the user. Can be NULL because there may be login providers that don't use emails.

| Property | Value |
| - | - |
|Type|nvarchar(254)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|yes|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Email](Sec_Users.md#email)|
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
|Max Length|254|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Email_Confirmed


Email_Confirmed


Indicates whether the email address for the specified user has been verified.


Indicates whether the email address for the specified user has been verified.

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
|Derived From|[Sec_Users](Sec_Users.md).[Email_Confirmed](Sec_Users.md#email_confirmed)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Lockout_End_Utc


Lockout_End_Utc


Contains the date and time (in UTC) until the user is locked. NULL when the user is not locked.


Contains the date and time (in UTC) until the user is locked. NULL when the user is not locked.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Lockout_End_Utc](Sec_Users.md#lockout_end_utc)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|GreaterThanOrLessThan|None|yes|no|
|Like|None|no|no|

### Password_Format


Password_Format


The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3.


The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`MD5`, `AN3`|
|Default Value|MD5|
|Derived From|[Sec_Users](Sec_Users.md).[Password_Format](Sec_Users.md#password_format)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Phone_Number


Phone_Number


Used only for two-factor authentication. NULL when phone-based two-factor is not used.


Used only for two-factor authentication. NULL when phone-based two-factor is not used.

| Property | Value |
| - | - |
|Type|nvarchar(64)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Phone_Number](Sec_Users.md#phone_number)|
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
|Max Length|64|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|
|Like|None|no|no|

### Phone_Number_Confirmed


Phone_Number_Confirmed


Indicates whether the Phone Number has been verified.


Indicates whether the Phone Number has been verified.

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
|Derived From|[Sec_Users](Sec_Users.md).[Phone_Number_Confirmed](Sec_Users.md#phone_number_confirmed)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Two_Factor_Enabled


Two_Factor_Enabled


Indicates whether two-factor authentication has been enabled.


Indicates whether two-factor authentication has been enabled.

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
|Derived From|[Sec_Users](Sec_Users.md).[Two_Factor_Enabled](Sec_Users.md#two_factor_enabled)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### User_Type


User_Type


Specifies the user type. INT=Internal; EXT=External (community); VIR=Virtual (No login); SYS=System; APP=Application.


Specifies the user type. INT=Internal; EXT=External (community); VIR=Virtual (No login); SYS=System; APP=Application.

| Property | Value |
| - | - |
|Type|nvarchar(3)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Allowed Values|`INT`, `EXT`, `VIR`, `SYS`, `APP`|
|Default Value|INT|
|Derived From|[Sec_Users](Sec_Users.md).[User_Type](Sec_Users.md#user_type)|
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
|Max Length|3|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Creation_Time_Utc


Creation_Time_Utc


The date and time (in UTC), when the user was created.


The date and time (in UTC), when the user was created.

| Property | Value |
| - | - |
|Type|datetime|
|DateTime Format|DateTime|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|yes|
|Sortable|no|
|Attributes|None|
|Default Value|CurrentDateTime|
|Derived From|[Sec_Users](Sec_Users.md).[Creation_Time_Utc](Sec_Users.md#creation_time_utc)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

### Domain_Id


Domain_Id


The domain, to which the user belongs.


The domain, to which the user belongs.

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Referenced Table|[Sec_Domains](Sec_Domains.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Domain_Id](Sec_Users.md#domain_id)|
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
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|yes|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|yes|no|

### Default_Culture


Default_Culture


The preferred default culture of the user for UI, notifications, etc. NULL means "en-US".


The preferred default culture of the user for UI, notifications, etc. NULL means "en-US".

| Property | Value |
| - | - |
|Type|nvarchar(15)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_Users](Sec_Users.md).[Default_Culture](Sec_Users.md#default_culture)|
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
|Max Length|15|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


