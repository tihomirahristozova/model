---
uid: Systems.Security.Users
---
# Systems.Security.Users Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

User logins. Entity: Sec_Users

## Default Visualization
Default Display Text Format:  
_{Login}_  
Default Search Member:  
_Login_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Security.Users](Systems.Security.Users.md)  
  * [Systems.Security.UserAccessKeys](Systems.Security.UserAccessKeys.md)  
  * [Systems.Security.UserGroups](Systems.Security.UserGroups.md)  
  * [Systems.Security.UserProviderLogins](Systems.Security.UserProviderLogins.md)  
  * [Systems.Security.UserProviderTokens](Systems.Security.UserProviderTokens.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessFailedCount](Systems.Security.Users.md#accessfailedcount) | int32 | Indicates how many times the user has failed to login. May be used for locking out the user. `Required` `Default(0)` `Filter(eq;ge;le)` `Introduced in version 18.2` 
| [Active](Systems.Security.Users.md#active) | boolean | True when the login is currently active and the user can log in. `Required` `Default(true)` `Filter(eq)` 
| [CreationTimeUtc](Systems.Security.Users.md#creationtimeutc) | datetime | The date and time (in UTC), when the user was created. `Required` `Default(Now)` `ReadOnly` `Introduced in version 18.2` 
| [DefaultCulture](Systems.Security.Users.md#defaultculture) | string (15) __nullable__ | The preferred default culture of the user for UI, notifications, etc. null means "en-US". `Introduced in version 20.1` 
| [Email](Systems.Security.Users.md#email) | string (254) __nullable__ | Unique email of the user. Can be null because there may be login providers that don't use emails. `Filter(multi eq;like)` `ORD` `Introduced in version 18.2` 
| [EmailConfirmed](Systems.Security.Users.md#emailconfirmed) | boolean | Indicates whether the email address for the specified user has been verified. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2` 
| [Id](Systems.Security.Users.md#id) | guid |  
| [IsAdmin](Systems.Security.Users.md#isadmin) | boolean | True if the user is administrator, otherwise false. `Required` `Default(false)` `Filter(eq)` 
| [LockoutEndUtc](Systems.Security.Users.md#lockoutendutc) | datetime __nullable__ | Contains the date and time (in UTC) until the user is locked. null when the user is not locked. `Filter(eq;ge;le;like)` `Introduced in version 18.2` 
| [Login](Systems.Security.Users.md#login) | string (64) | The login name of the user, which is usually the email. `Required` `Filter(multi eq;like)` `ORD` 
| [Name](Systems.Security.Users.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The full name of the user. `Required` `Filter(like)` 
| [Notes](Systems.Security.Users.md#notes) | string (254) __nullable__ | Notes for this User. 
| [Password](Systems.Security.Users.md#password) | string (64) __nullable__ | The password hash of the user, stored in the format, specified in Password Format. 
| [PasswordFormat](Systems.Security.Users.md#passwordformat) | [PasswordFormat](Systems.Security.Users.md#passwordformat) | The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3. `Required` `Default("MD5")` `Filter(eq)` `Introduced in version 18.2` 
| [PhoneNumber](Systems.Security.Users.md#phonenumber) | string (64) __nullable__ | Used only for two-factor authentication. null when phone-based two-factor is not used. `Filter(eq;like)` `Introduced in version 18.2` 
| [PhoneNumberConfirmed](Systems.Security.Users.md#phonenumberconfirmed) | boolean | Indicates whether the Phone Number has been verified. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2` 
| [TwoFactorEnabled](Systems.Security.Users.md#twofactorenabled) | boolean | Indicates whether two-factor authentication has been enabled. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2` 
| [UserType](Systems.Security.Users.md#usertype) | [UserType](Systems.Security.Users.md#usertype) | Specifies the user type. INT=Internal; EXT=External (community); VIR=Virtual (No login); SYS=System; APP=Application. `Required` `Default("INT")` `Filter(multi eq)` `Introduced in version 18.2` 
| [VoiceExtensionNumbers](Systems.Security.Users.md#voiceextensionnumbers) | string (254) __nullable__ | Comma separated list of internal extension numbers of the voice telephones of the user. Used for VOIP integration. 
| [WindowsUserName](Systems.Security.Users.md#windowsusername) | string (128) __nullable__ | The Windows (Active Directory) user, to which this login is bound. The user will be allowed to login only when the client machine is logged in Active Directory with the specified user. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Domain](Systems.Security.Users.md#domain) | [Domains](Systems.Security.Domains.md) (nullable) | The domain, to which the user belongs. `Filter(multi eq)` `Introduced in version 20.1` |
| [Person](Systems.Security.Users.md#person) | [Persons](General.Contacts.Persons.md) (nullable) | The person from within the system, which is authenticated with this login. null means that this user is not associated with a person record in the database. `Filter(multi eq)` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| AccessKeys | [UserAccessKeys](Systems.Security.UserAccessKeys.md) | List of `UserAccessKey`(Systems.Security.UserAccessKeys.md) child objects, based on the `Systems.Security.UserAccessKey.User`(Systems.Security.UserAccessKeys.md#user) back reference 
| Groups | [UserGroups](Systems.Security.UserGroups.md) | List of `UserGroup`(Systems.Security.UserGroups.md) child objects, based on the `Systems.Security.UserGroup.User`(Systems.Security.UserGroups.md#user) back reference 
| ProviderLogins | [UserProviderLogins](Systems.Security.UserProviderLogins.md) | List of `UserProviderLogin`(Systems.Security.UserProviderLogins.md) child objects, based on the `Systems.Security.UserProviderLogin.User`(Systems.Security.UserProviderLogins.md#user) back reference 
| ProviderTokens | [UserProviderTokens](Systems.Security.UserProviderTokens.md) | List of `UserProviderToken`(Systems.Security.UserProviderTokens.md) child objects, based on the `Systems.Security.UserProviderToken.User`(Systems.Security.UserProviderTokens.md#user) back reference 


## Attribute Details

### AccessFailedCount

Indicates how many times the user has failed to login. May be used for locking out the user. `Required` `Default(0)` `Filter(eq;ge;le)` `Introduced in version 18.2`

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **0**  

### Active

True when the login is currently active and the user can log in. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### CreationTimeUtc

The date and time (in UTC), when the user was created. `Required` `Default(Now)` `ReadOnly` `Introduced in version 18.2`

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### DefaultCulture

The preferred default culture of the user for UI, notifications, etc. null means "en-US". `Introduced in version 20.1`

_Type_: **string (15) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **15**  

### Email

Unique email of the user. Can be null because there may be login providers that don't use emails. `Filter(multi eq;like)` `ORD` `Introduced in version 18.2`

_Type_: **string (254) __nullable__**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **254**  

### EmailConfirmed

Indicates whether the email address for the specified user has been verified. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsAdmin

True if the user is administrator, otherwise false. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LockoutEndUtc

Contains the date and time (in UTC) until the user is locked. null when the user is not locked. `Filter(eq;ge;le;like)` `Introduced in version 18.2`

_Type_: **datetime __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, Like**  
_Supports Order By_: **False**  

### Login

The login name of the user, which is usually the email. `Required` `Filter(multi eq;like)` `ORD`

_Type_: **string (64)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **64**  

### Name

The full name of the user. `Required` `Filter(like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

Notes for this User.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Password

The password hash of the user, stored in the format, specified in Password Format.

_Type_: **string (64) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PasswordFormat

The format of the Password. MD5=MD5 format; AN3 = ASP.NET Core Identity v3. `Required` `Default("MD5")` `Filter(eq)` `Introduced in version 18.2`

_Type_: **[PasswordFormat](Systems.Security.Users.md#passwordformat)**  
Allowed values for the `PasswordFormat`(Systems.Security.Users.md#passwordformat) data attribute  
_Allowed Values (Systems.Security.UsersRepository.PasswordFormat Enum Members)_  

| Value | Description |
| ---- | --- |
| MD5 | Store password in the old format, used by the Windows App. Stored as 'MD5'. <br /> _Database Value:_ 'MD5' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'MD5' |
| AspNetCoreV3 | Store passwords in v3 format used by ASP.NET Core. Stored as 'AN3'. <br /> _Database Value:_ 'AN3' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'AspNetCoreV3' |

_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **MD5**  

### PhoneNumber

Used only for two-factor authentication. null when phone-based two-factor is not used. `Filter(eq;like)` `Introduced in version 18.2`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### PhoneNumberConfirmed

Indicates whether the Phone Number has been verified. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### TwoFactorEnabled

Indicates whether two-factor authentication has been enabled. `Required` `Default(false)` `Filter(eq)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### UserType

Specifies the user type. INT=Internal; EXT=External (community); VIR=Virtual (No login); SYS=System; APP=Application. `Required` `Default("INT")` `Filter(multi eq)` `Introduced in version 18.2`

_Type_: **[UserType](Systems.Security.Users.md#usertype)**  
Allowed values for the `UserType`(Systems.Security.Users.md#usertype) data attribute  
_Allowed Values (Systems.Security.UsersRepository.UserType Enum Members)_  

| Value | Description |
| ---- | --- |
| InternalUser | Internal users are the usual ERP users. They have access to internal and external content.. Stored as 'INT'. <br /> _Database Value:_ 'INT' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'InternalUser' |
| ExternalCommunityUser | External users can access only external (community) content. They are usually created withing community sites.. Stored as 'EXT'. <br /> _Database Value:_ 'EXT' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'ExternalCommunityUser' |
| VirtualUserNoLogin | Virtual users cannot login, but can be used for task assignments, etc.. Stored as 'VIR'. <br /> _Database Value:_ 'VIR' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'VirtualUserNoLogin' |
| SystemUserNoLogin | System users are used only by local system applications.. Stored as 'SYS'. <br /> _Database Value:_ 'SYS' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'SystemUserNoLogin' |
| ApplicationUserNoLogin | Application users are used by applications. They do not have a password, but login by providing application credentials.. Stored as 'APP'. <br /> _Database Value:_ 'APP' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'ApplicationUserNoLogin' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **InternalUser**  

### VoiceExtensionNumbers

Comma separated list of internal extension numbers of the voice telephones of the user. Used for VOIP integration.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### WindowsUserName

The Windows (Active Directory) user, to which this login is bound. The user will be allowed to login only when the client machine is logged in Active Directory with the specified user.

_Type_: **string (128) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  


## Reference Details

### Domain

The domain, to which the user belongs. `Filter(multi eq)` `Introduced in version 20.1`

_Type_: **[Domains](Systems.Security.Domains.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

The person from within the system, which is authenticated with this login. null means that this user is not associated with a person record in the database. `Filter(multi eq)`

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Security.Users erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.Users erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_Users?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_Users?$top=10>

