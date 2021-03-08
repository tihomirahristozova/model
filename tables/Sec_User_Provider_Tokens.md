# Table Sec_User_Provider_Tokens

Stores verification tokens for users - e.g. tokens for email, phone or two-factor authentication. Entity: Sec_User_Provider_Tokens (Introduced in version 18.2)

# Aggregate Hierarchy

* [Sec_Users](Sec_Users.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Provider_Token_Id|`Guid`|`PK`, Readonly||
|Login_Provider_Name|`String`||Name of the login provider. Could be Facebook, Twitter, E1UserStore, etc. `Required` `Filter(eq)` |
|Token_Name|`String`||What kind of token we store, Could be (but is not limited to): AuthenticatorKey (two-factor auth), RecoveryCodes (password recovery). `Required` `Filter(eq)` |
|Token_Value|`String`||Actual value depends on Login_Provider_Name and Token_Name. Could be null because the presence of (User_Id, Login_Provider_Name and Token_Name) might be enough for some providers. |
