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


User_Provider_Token_Id


Primary key - not used


Primary key - not used

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
|Derived From|[Sec_User_Provider_Tokens](Sec_User_Provider_Tokens.md).[User_Provider_Token_Id](Sec_User_Provider_Tokens.md#user_provider_token_id)|
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
|Equals|NULL|no|no|

### User_Id


User_Id


User for which we store tokens


User for which we store tokens

| Property | Value |
| - | - |
|Type|uniqueidentifier|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|yes|
|Referenced Table|[Sec_Users](Sec_Users.md)|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_User_Provider_Tokens](Sec_User_Provider_Tokens.md).[User_Id](Sec_User_Provider_Tokens.md#user_id)|
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
|Equals|NULL|no|no|

### Login_Provider_Name


Login_Provider_Name


Name of the login provider. Could be Facebook, Twitter, E1UserStore, etc


Name of the login provider. Could be Facebook, Twitter, E1UserStore, etc

| Property | Value |
| - | - |
|Type|nvarchar(450)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_User_Provider_Tokens](Sec_User_Provider_Tokens.md).[Login_Provider_Name](Sec_User_Provider_Tokens.md#login_provider_name)|
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
|Max Length|450|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Token_Name


Token_Name


What kind of token we store, Could be (but is not limited to): AuthenticatorKey (two-factor auth), RecoveryCodes (password recovery)


What kind of token we store, Could be (but is not limited to): AuthenticatorKey (two-factor auth), RecoveryCodes (password recovery)

| Property | Value |
| - | - |
|Type|nvarchar(450)|
|Is Mulitlanguage|no|
|`NULL`|no|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_User_Provider_Tokens](Sec_User_Provider_Tokens.md).[Token_Name](Sec_User_Provider_Tokens.md#token_name)|
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
|Max Length|450|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|

#### Supported Filters

| Filter Type | Default |Include Nulls | Hidden by Default |
| - | - | - | - |
|Equals|NULL|no|no|

### Token_Value


Token_Value


Actual value depends on Login_Provider_Name and Token_Name. Could be null because the presence of (User_Id, Login_Provider_Name and Token_Name) might be enough for some providers.


Actual value depends on Login_Provider_Name and Token_Name. Could be null because the presence of (User_Id, Login_Provider_Name and Token_Name) might be enough for some providers.

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|
|Is Mulitlanguage|no|
|`NULL`|yes|
|Primary Key|no|
|Ownership Reference|no|
|Readonly|no|
|Sortable|no|
|Attributes|None|
|Default Value|None|
|Derived From|[Sec_User_Provider_Tokens](Sec_User_Provider_Tokens.md).[Token_Value](Sec_User_Provider_Tokens.md#token_value)|
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
|Max Length|2147483647|
|Order|2147483647|
|Summary Type|None|
|UI Memo Editor|no|
|UI Width|Medium|
|Supports EQUALS_IN|no|


