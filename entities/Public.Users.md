---
uid: Public.Users
---
# Public.Users View

**Namespace:** [Public](Public.md)  

Public users profile data. Entity: Public_Users (Introduced in version 22.1.4.22)

## Default Visualization
Default Display Text Format:  
_{Name}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Public.Users](Public.Users.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Email](Public.Users.md#email) | string (254) __nullable__ | Unique email of the user. Can be null because there may be login providers that don't use emails. `Filter(multi eq;like)` `Inherited from Sec_Users_Table.Email` 
| [IsAdmin](Public.Users.md#isadmin) | boolean | True if the user is administrator, otherwise false. `Required` `Default(false)` `Filter(eq)` `Inherited from Sec_Users_Table.Is_Admin` 
| [Login](Public.Users.md#login) | string (64) | The login name of the user, which is usually the email. `Required` `Filter(multi eq;like)` `Inherited from Sec_Users_Table.Login` 
| [Name](Public.Users.md#name) | [MultilanguageString (254)](../data-types.md#multilanguagestring) | The full name of the user. `Required` `Filter(like)` `Inherited from Sec_Users_Table.User_Name` 
| [UserId](Public.Users.md#userid) | guid | The Id of the security user. `Required` `Filter(multi eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Person](Public.Users.md#person) | [Persons](General.Contacts.Persons.md) (nullable) | The person from within the system, which is authenticated with this login. null means that this user is not associated with a person record in the database. `Filter(multi eq)` `Inherited from Sec_Users_Table.Person_Id` |


## Attribute Details

### Email

Unique email of the user. Can be null because there may be login providers that don't use emails. `Filter(multi eq;like)` `Inherited from Sec_Users_Table.Email`

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Inherited From_: **Sec_Users_Table.Email**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### IsAdmin

True if the user is administrator, otherwise false. `Required` `Default(false)` `Filter(eq)` `Inherited from Sec_Users_Table.Is_Admin`

_Type_: **boolean**  
_Category_: **System**  
_Inherited From_: **Sec_Users_Table.Is_Admin**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Login

The login name of the user, which is usually the email. `Required` `Filter(multi eq;like)` `Inherited from Sec_Users_Table.Login`

_Type_: **string (64)**  
_Category_: **System**  
_Inherited From_: **Sec_Users_Table.Login**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### Name

The full name of the user. `Required` `Filter(like)` `Inherited from Sec_Users_Table.User_Name`

_Type_: **[MultilanguageString (254)](../data-types.md#multilanguagestring)**  
_Category_: **System**  
_Inherited From_: **Sec_Users_Table.User_Name**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### UserId

The Id of the security user. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  


## Reference Details

### Person

The person from within the system, which is authenticated with this login. null means that this user is not associated with a person record in the database. `Filter(multi eq)` `Inherited from Sec_Users_Table.Person_Id`

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Category_: **System**  
_Inherited From_: **Sec_Users_Table.Person_Id**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAccessKeyPermissions

Gets the permissions this user has to access resources protected by the provided access key.  
_Return Type_: **[SecurityPermissions](../data-types.md#systems.security.securitypermissions)**  
_Declaring Type_: **[Users](Public.Users.md)**  
_Domain API Request_: **POST**  

**Parameters**  
  * **accessKeyId**  
    The access key id  
    _Type_: guid  

  * **idToken**  
    The identity token of the logged in user. Required when the currently logged user is different from the public user.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  


## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Public_Users?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Public_Users?$top=10>

