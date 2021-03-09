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

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Login

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### User_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Password

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Is_Admin

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Active

| Property | Value |
| - | - |
|Type|bit|

### Windows_User_Name

| Property | Value |
| - | - |
|Type|nvarchar(128)|

### Voice_Extension_Numbers

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|

### Access_Failed_Count

| Property | Value |
| - | - |
|Type|int|

### Email

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Email_Confirmed

| Property | Value |
| - | - |
|Type|bit|

### Lockout_End_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Password_Format

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Phone_Number

| Property | Value |
| - | - |
|Type|nvarchar(64)|

### Phone_Number_Confirmed

| Property | Value |
| - | - |
|Type|bit|

### Two_Factor_Enabled

| Property | Value |
| - | - |
|Type|bit|

### User_Type

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Creation_Time_Utc

| Property | Value |
| - | - |
|Type|datetime|

### Domain_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Default_Culture

| Property | Value |
| - | - |
|Type|nvarchar(15)|


