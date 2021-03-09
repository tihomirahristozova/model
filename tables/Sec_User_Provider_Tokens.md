# Table Sec_User_Provider_Tokens

Stores verification tokens for users - e.g. tokens for email, phone or two-factor authentication. Entity: Sec_User_Provider_Tokens (Introduced in version 18.2)

## Owner Tables Hierarchy

* [Sec_Users](Sec_Users.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[User_Provider_Token_Id](#user_provider_token_id)|`uniqueidentifier` `PK`|Primary key - not used|
|[User_Id](#user_id)|`uniqueidentifier` |User for which we store tokens|
|[Login_Provider_Name](#login_provider_name)|`nvarchar(450)` |Name of the login provider. Could be Facebook, Twitter, E1UserStore, etc|
|[Token_Name](#token_name)|`nvarchar(450)` |What kind of token we store, Could be (but is not limited to): AuthenticatorKey (two-factor auth), RecoveryCodes (password recovery)|
|[Token_Value](#token_value)|`nvarchar(2147483647)` |Actual value depends on Login_Provider_Name and Token_Name. Could be null because the presence of (User_Id, Login_Provider_Name and Token_Name) might be enough for some providers.|

## Columns

### User_Provider_Token_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### User_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Login_Provider_Name

| Property | Value |
| - | - |
|Type|nvarchar(450)|

### Token_Name

| Property | Value |
| - | - |
|Type|nvarchar(450)|

### Token_Value

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


