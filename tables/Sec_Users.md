# Table Sec_Users

User logins. Entity: Sec_Users

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|User_Id|`Guid`|`PK`, Readonly||
|Access_Failed_Count|`Int32`||Indicates how many times the user has failed to login. May be used for locking out the user. `Required` `Default(0)` `Filter(eq;ge;le)` `Introduced in version 18.2` |
|Active|`Boolean`||True when the login is currently active and the user can log in. `Required` `Default(true)` `Filter(eq)` |
|Creation_Time_Utc|`DateTime`|Readonly|The date and time (in UTC), when the user was created. `Required` `Default(Now)` `ReadOnly` `Introduced in version 18.2` |
|Default_Culture|`String`||The preferred default culture of the user for UI, notifications, etc. null means "en-US". `Introduced in version 20.1` |
|Email|`String`||Unique email of the user. Can be null because there may be login providers that don't use emails. `Filter(multi eq;like)` `ORD` `Introduced in version 18.2` |
|Email_Confirmed|`Boolean`||Indicates whether the email address for the specified user has been verified. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2` |
|Is_Admin|`Boolean`||True if the user is administrator, otherwise false. `Required` `Default(false)` `Filter(eq)` |
|Lockout_End_Utc|`DateTime?`||Contains the date and time (in UTC) until the user is locked. null when the user is not locked. `Filter(eq;ge;le;like)` `Introduced in version 18.2` |
|Login|`String`||The login name of the user, which is usually the email. `Required` `Filter(multi eq;like)` `ORD` |
|User_Name|`MultilanguageString`||The full name of the user. `Required` `Filter(like)` |
|Notes|`String`||Notes for this User. |
|Password|`String`||The password hash of the user, stored in the format, specified in Password Format. |
|Password_Format|`PasswordFormat`|Allowed: `MD5`, `AN3`|The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3. `Required` `Default("MD5")` `Filter(eq)` `Introduced in version 18.2` |
|Phone_Number|`String`||Used only for two-factor authentication. null when phone-based two-factor is not used. `Filter(eq;like)` `Introduced in version 18.2` |
|Phone_Number_Confirmed|`Boolean`||Indicates whether the Phone Number has been verified. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2` |
|Two_Factor_Enabled|`Boolean`||Indicates whether two-factor authentication has been enabled. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2` |
|User_Type|`UserType`|Allowed: `INT`, `EXT`, `VIR`, `SYS`, `APP`|Specifies the user type. INT=Internal; EXT=External (community); VIR=Virtual (No login); SYS=System; APP=Application. `Required` `Default("INT")` `Filter(multi eq)` `Introduced in version 18.2` |
|Voice_Extension_Numbers|`String`||Comma separated list of internal extension numbers of the voice telephones of the user. Used for VOIP integration. |
|Windows_User_Name|`String`||The Windows (Active Directory) user, to which this login is bound. The user will be allowed to login only when the client machine is logged in Active Directory with the specified user. |
