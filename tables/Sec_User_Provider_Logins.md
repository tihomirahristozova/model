# Table Sec_User_Provider_Logins

External login providers. Entity: Sec_User_Provider_Logins (Introduced in version 18.2)

# Aggregate Hierarchy

* [Sec_Users](Sec_Users.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Provider_Login_Id|`Guid`|`PK`, Readonly||
|Provider_Key|`String`||The key, which the provider provided for logging the user. `Required` `Filter(multi eq)` |
|Provider_Name|`ProviderName`|Allowed: `ERPNET`, `GOOGLE`, `FACEBOOK`|The system name of the authentication provider. It should be already registered for the domain. `Required` `Filter(eq)` `Introduced in version 20.1` |
