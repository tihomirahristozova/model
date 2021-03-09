# Query Sec_Users_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Id](#user_id)|`uniqueidentifier` `PK`||
|[Login](#login)|`nvarchar` ||
|[User_Name](#user_name)|`nvarchar` `ML`||
|[Is_Admin](#is_admin)|`bit` ||
|[Notes](#notes)|`nvarchar` ||
|[Person_Id](#person_id)|`uniqueidentifier` ||
|[Active](#active)|`bit` ||
|[Windows_User_Name](#windows_user_name)|`nvarchar` ||
|[Voice_Extension_Numbers](#voice_extension_numbers)|`nvarchar` ||
|[Access_Failed_Count](#access_failed_count)|`int` |Indicates how many times the user has failed to login with valid credentials. May be used for locking out the user.|
|[Email](#email)|`nvarchar` |Unique email of the user. Can be NULL because there may be login providers that don't use emails.|
|[Email_Confirmed](#email_confirmed)|`bit` |Indicates whether the email address for the specified user has been verified.|
|[Lockout_End_Utc](#lockout_end_utc)|`datetime` |Contains the date and time (in UTC) until the user is locked. NULL when the user is not locked.|
|[Password_Format](#password_format)|`nvarchar` Allowed: `MD5`, `AN3`|The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3.|
|[Phone_Number](#phone_number)|`nvarchar` |Used only for two-factor authentication. NULL when phone-based two-factor is not used.|
|[Phone_Number_Confirmed](#phone_number_confirmed)|`bit` |Indicates whether the Phone Number has been verified.|
|[Two_Factor_Enabled](#two_factor_enabled)|`bit` |Indicates whether two-factor authentication has been enabled.|
|[User_Type](#user_type)|`nvarchar` Allowed: `INT`, `EXT`, `VIR`, `SYS`, `APP`|Specifies the user type. Internal users have access to internal and external content. External users can access only external (community) content. Virtual users cannot login, but can be used for task assignments, etc. I=Internal; E=External; V=Virtual.|
|[Creation_Time_Utc](#creation_time_utc)|`datetime` |The date and time (in UTC) when the user was created.|
|[Domain_Id](#domain_id)|`uniqueidentifier` |The domain, to which the user belongs.|
|[Default_Culture](#default_culture)|`nvarchar` |The preferred default culture of the user for UI, notifications, etc. NULL means "en-US".|

## Columns

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Login

| Property | Value |
| - | - |
|Type|nvarchar|

### User_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Is_Admin

| Property | Value |
| - | - |
|Type|bit|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Voice_Extension_Numbers

| Property | Value |
| - | - |
|Type|nvarchar|

### Access_Failed_Count

| Property | Value |
| - | - |
|Type|int|

### Email

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

### Phone_Number

| Property | Value |
| - | - |
|Type|nvarchar|

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
|Type|nvarchar|

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
|Type|nvarchar|


