# Table Sec_User_Provider_Logins

External login providers. Entity: Sec_User_Provider_Logins (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Sec_Users](Sec_Users.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Provider_Login_Id](#user_provider_login_id)|`uniqueidentifier` `PK`||
|[User_Id](#user_id)|`uniqueidentifier` |The user for which the login is defined.|
|[Provider_Name](#provider_name)|`nvarchar(50)` Allowed: `ERPNET`, `GOOGLE`, `FACEBOOK`|The system name of the authentication provider. It should be already registered for the domain.|
|[Provider_Key](#provider_key)|`nvarchar(450)` |The key, which the provider provided for logging the user.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### User_Provider_Login_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Provider_Name

| Property | Value |
| - | - |
|Type|nvarchar(50)|

### Provider_Key

| Property | Value |
| - | - |
|Type|nvarchar(450)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


