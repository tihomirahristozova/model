---
uid: Systems.External.PublicUsers
---
# Systems.External.PublicUsers Entity

**Namespace:** [Systems.External](Systems.External.md)  

/Users of the publicly offered services. This includes Internet, external and employee users. Entity: Ext_Public_Users

## Default Visualization
Default Display Text Format:  
_{PhoneNumber}: {CompanyName:T}_  
Default Search Member:  
_PhoneNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.External.PublicUsers](Systems.External.PublicUsers.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AboutMeText](Systems.External.PublicUsers.md#aboutmetext) | string(1024) (nullable) | About me text, written by the user. 
| [Address](Systems.External.PublicUsers.md#address) | string(128) (nullable) | The primary address of the user. Can be specified with latin or local characters. `Filter(like)` 
| [AlternateEmail](Systems.External.PublicUsers.md#alternateemail) | string(64) (nullable) | Alternate email of the user. Can be used for backup email for password restore. `Filter(like)` 
| [City](Systems.External.PublicUsers.md#city) | string(64) (nullable) | The state of residence of the user. Can be specified with latin or local letters. `Filter(like)` 
| [CompanyName](Systems.External.PublicUsers.md#companyname) | string(64) (nullable) | The name of the company, for which the user works, as specified by the user. `Filter(like)` 
| [Country](Systems.External.PublicUsers.md#country) | string(64) (nullable) | The country of residence of the user, with latin letters. `Filter(like)` 
| [CreatedOn](Systems.External.PublicUsers.md#createdon) | datetime (nullable) | The date and time when the user was created. `Default(Now)` 
| [Email](Systems.External.PublicUsers.md#email) | string(64) | The primary email of the user. Used for notifications and password restore. `Required` `Filter(like)` 
| [FirstName](Systems.External.PublicUsers.md#firstname) | string(64) | First name of the user. `Required` `Filter(like)` 
| [Id](Systems.External.PublicUsers.md#id) | guid |  
| [IsActive](Systems.External.PublicUsers.md#isactive) | boolean | Specifies whether the user account is active and access should be allowed. `Required` `Default(true)` `Filter(eq)` 
| [LastName](Systems.External.PublicUsers.md#lastname) | string(64) | Last name of the user. `Required` `Filter(like)` 
| [Notes](Systems.External.PublicUsers.md#notes) | string(2147483647) (nullable) | Notes for this PublicUser. 
| [PasswordAlgorithm](Systems.External.PublicUsers.md#passwordalgorithm) | string(16) | Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'. `Required` `Filter(like)` 
| [PasswordHash](Systems.External.PublicUsers.md#passwordhash) | string(128) | Actual password storage. The format of the contents is determined by Password Algorithm. `Required` `Filter(like)` 
| [PasswordRecoveryCode](Systems.External.PublicUsers.md#passwordrecoverycode) | guid (nullable) | Automatically generated unique code for the last password recovery attempt. `Filter(multi eq)` `ReadOnly` 
| [PasswordRecovery<br />CreationTime](Systems.External.PublicUsers.md#passwordrecoverycreationtime) | datetime (nullable) | Date and time when the last password recovery code was created. `ReadOnly` 
| [PhoneNumber](Systems.External.PublicUsers.md#phonenumber) | string(16) (nullable) | The primary phone number of the user. `Filter(like)` 
| [PostalCode](Systems.External.PublicUsers.md#postalcode) | string(16) (nullable) | The postal code of the default address of the user. `Filter(like)` 
| [ProfilePicture](Systems.External.PublicUsers.md#profilepicture) | byte[] (nullable) | Profile picture of the user. 
| [State](Systems.External.PublicUsers.md#state) | string(64) (nullable) | The state of residence of the user within the country. Can be specified with latin or local characters. `Filter(like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Company](Systems.External.PublicUsers.md#company) | [Companies](General.Contacts.Companies.md) (nullable) | Link to an internal company record, specified by internal employee. `Filter(multi eq)` |
| [Person](Systems.External.PublicUsers.md#person) | [Persons](General.Contacts.Persons.md) (nullable) | Link to an internal person record. Usually specified by internal employee, but can also be an automated process. `Filter(multi eq)` |
| [PublicUserList](Systems.External.PublicUsers.md#publicuserlist) | [PublicUserLists](Systems.External.PublicUserLists.md) | The list in which the user account is saved. `Required` `Filter(multi eq)` |


## Attribute Details

### AboutMeText

About me text, written by the user.

_Type_: **string(1024) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **1024**  

### Address

The primary address of the user. Can be specified with latin or local characters. `Filter(like)`

_Type_: **string(128) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### AlternateEmail

Alternate email of the user. Can be used for backup email for password restore. `Filter(like)`

_Type_: **string(64) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### City

The state of residence of the user. Can be specified with latin or local letters. `Filter(like)`

_Type_: **string(64) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### CompanyName

The name of the company, for which the user works, as specified by the user. `Filter(like)`

_Type_: **string(64) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Country

The country of residence of the user, with latin letters. `Filter(like)`

_Type_: **string(64) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### CreatedOn

The date and time when the user was created. `Default(Now)`

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Email

The primary email of the user. Used for notifications and password restore. `Required` `Filter(like)`

_Type_: **string(64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### FirstName

First name of the user. `Required` `Filter(like)`

_Type_: **string(64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the user account is active and access should be allowed. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LastName

Last name of the user. `Required` `Filter(like)`

_Type_: **string(64)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Notes

Notes for this PublicUser.

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### PasswordAlgorithm

Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'. `Required` `Filter(like)`

_Type_: **string(16)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### PasswordHash

Actual password storage. The format of the contents is determined by Password Algorithm. `Required` `Filter(like)`

_Type_: **string(128)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **128**  

### PasswordRecoveryCode

Automatically generated unique code for the last password recovery attempt. `Filter(multi eq)` `ReadOnly`

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PasswordRecoveryCreationTime

Date and time when the last password recovery code was created. `ReadOnly`

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PhoneNumber

The primary phone number of the user. `Filter(like)`

_Type_: **string(16) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### PostalCode

The postal code of the default address of the user. `Filter(like)`

_Type_: **string(16) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### ProfilePicture

Profile picture of the user.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### State

The state of residence of the user within the country. Can be specified with latin or local characters. `Filter(like)`

_Type_: **string(64) (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  


## Reference Details

### Company

Link to an internal company record, specified by internal employee. `Filter(multi eq)`

_Type_: **[Companies](General.Contacts.Companies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

Link to an internal person record. Usually specified by internal employee, but can also be an automated process. `Filter(multi eq)`

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### PublicUserList

The list in which the user account is saved. `Required` `Filter(multi eq)`

_Type_: **[PublicUserLists](Systems.External.PublicUserLists.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.External.PublicUsers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.External.PublicUsers erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_External_PublicUsers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_External_PublicUsers?$top=10>

