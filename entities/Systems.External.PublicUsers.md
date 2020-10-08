---
uid: Systems.External.PublicUsers
---
# Systems.External.PublicUsers

/Users of the publicly offered services. This includes Internet, external and employee users. Entity: Ext_Public_Users

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.External.PublicUsers.md#Id) | guid |  
| [AboutMeText](Systems.External.PublicUsers.md#AboutMeText) | string (nullable) | About me text, written by the user. 
| [Address](Systems.External.PublicUsers.md#Address) | string (nullable) | The primary address of the user. Can be specified with latin or local characters. [Filter(like)] 
| [AlternateEmail](Systems.External.PublicUsers.md#AlternateEmail) | string (nullable) | Alternate email of the user. Can be used for backup email for password restore. [Filter(like)] 
| [City](Systems.External.PublicUsers.md#City) | string (nullable) | The state of residence of the user. Can be specified with latin or local letters. [Filter(like)] 
| [CompanyName](Systems.External.PublicUsers.md#CompanyName) | string (nullable) | The name of the company, for which the user works, as specified by the user. [Filter(like)] 
| [Country](Systems.External.PublicUsers.md#Country) | string (nullable) | The country of residence of the user, with latin letters. [Filter(like)] 
| [CreatedOn](Systems.External.PublicUsers.md#CreatedOn) | datetime (nullable) | The date and time when the user was created. [Default(Now)] 
| [Email](Systems.External.PublicUsers.md#Email) | string | The primary email of the user. Used for notifications and password restore. [Required] [Filter(like)] 
| [FirstName](Systems.External.PublicUsers.md#FirstName) | string | First name of the user. [Required] [Filter(like)] 
| [IsActive](Systems.External.PublicUsers.md#IsActive) | boolean | Specifies whether the user account is active and access should be allowed. [Required] [Default(true)] [Filter(eq)] 
| [LastName](Systems.External.PublicUsers.md#LastName) | string | Last name of the user. [Required] [Filter(like)] 
| [Notes](Systems.External.PublicUsers.md#Notes) | string (nullable) | Notes for this PublicUser. 
| [PasswordAlgorithm](Systems.External.PublicUsers.md#PasswordAlgorithm) | string | Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'. [Required] [Filter(like)] 
| [PasswordHash](Systems.External.PublicUsers.md#PasswordHash) | string | Actual password storage. The format of the contents is determined by Password Algorithm. [Required] [Filter(like)] 
| [PasswordRecoveryCode](Systems.External.PublicUsers.md#PasswordRecoveryCode) | guid (nullable) | Automatically generated unique code for the last password recovery attempt. [Filter(multi eq)] [ReadOnly] 
| [PasswordRecoveryCreationTime](Systems.External.PublicUsers.md#PasswordRecoveryCreationTime) | datetime (nullable) | Date and time when the last password recovery code was created. [ReadOnly] 
| [PhoneNumber](Systems.External.PublicUsers.md#PhoneNumber) | string (nullable) | The primary phone number of the user. [Filter(like)] 
| [PostalCode](Systems.External.PublicUsers.md#PostalCode) | string (nullable) | The postal code of the default address of the user. [Filter(like)] 
| [ProfilePicture](Systems.External.PublicUsers.md#ProfilePicture) | byte[] (nullable) | Profile picture of the user. 
| [State](Systems.External.PublicUsers.md#State) | string (nullable) | The state of residence of the user within the country. Can be specified with latin or local characters. [Filter(like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Company](Systems.External.PublicUsers.md#Company) | [General.Contacts.Companies](General.Contacts.Companies.md) (nullable) | Link to an internal company record, specified by internal employee. [Filter(multi eq)] |
| [Person](Systems.External.PublicUsers.md#Person) | [General.Contacts.Persons](General.Contacts.Persons.md) (nullable) | Link to an internal person record. Usually specified by internal employee, but can also be an automated process. [Filter(multi eq)] |
| [PublicUserList](Systems.External.PublicUsers.md#PublicUserList) | [Systems.External.PublicUserLists](Systems.External.PublicUserLists.md) | The list in which the user account is saved. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### AboutMeText

> About me text, written by the user.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Address

> The primary address of the user. Can be specified with latin or local characters. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### AlternateEmail

> Alternate email of the user. Can be used for backup email for password restore. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### City

> The state of residence of the user. Can be specified with latin or local letters. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CompanyName

> The name of the company, for which the user works, as specified by the user. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Country

> The country of residence of the user, with latin letters. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### CreatedOn

> The date and time when the user was created. [Default(Now)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Email

> The primary email of the user. Used for notifications and password restore. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### FirstName

> First name of the user. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### IsActive

> Specifies whether the user account is active and access should be allowed. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LastName

> Last name of the user. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this PublicUser.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PasswordAlgorithm

> Uniquely specifies the password storage algorithm among some system recognized algorithms. Usually specifies the hashing and the stretching functions. For example, 'PBKDF2-SHA1'. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### PasswordHash

> Actual password storage. The format of the contents is determined by Password Algorithm. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### PasswordRecoveryCode

> Automatically generated unique code for the last password recovery attempt. [Filter(multi eq)] [ReadOnly]

_Type_: **guid (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PasswordRecoveryCreationTime

> Date and time when the last password recovery code was created. [ReadOnly]

_Type_: **datetime (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PhoneNumber

> The primary phone number of the user. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### PostalCode

> The postal code of the default address of the user. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### ProfilePicture

> Profile picture of the user.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### State

> The state of residence of the user within the country. Can be specified with latin or local characters. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  


## Reference Details

### Company

> Link to an internal company record, specified by internal employee. [Filter(multi eq)]

_Type_: **[General.Contacts.Companies](General.Contacts.Companies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Person

> Link to an internal person record. Usually specified by internal employee, but can also be an automated process. [Filter(multi eq)]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### PublicUserList

> The list in which the user account is saved. [Required] [Filter(multi eq)]

_Type_: **[Systems.External.PublicUserLists](Systems.External.PublicUserLists.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.External.PublicUsers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.External.PublicUsers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.External.PublicUsers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_External_PublicUsers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_External_PublicUsers?$top=10>

