---
uid: Public.Users
---
# Public.Users View

**Namespace:** [Public](Public.md)  

Public users profile data. Entity: Public_Users (Introduced in version 22.1.4.22)

## Default Visualization
Default Display Text Format:  
_{UserId}: {Email}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Public.Users](Public.Users.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Email](Public.Users.md#email) | string (254) | Unique email of the user. Can be null because there may be login providers that don't use emails. `Required` 
| [Name](Public.Users.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The full name of the user. `Required` 
| [UserId](Public.Users.md#userid) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Person](Public.Users.md#person) | [Persons](General.Contacts.Persons.md) | The person from within the system, which is authenticated with this login. null means that this user is not associated with a person record in the database. `Required` `Default(New Guid)` `Filter(multi eq)` `Inherited from Cm_Persons_Table.Person_Id` |


## Attribute Details

### Email

Unique email of the user. Can be null because there may be login providers that don't use emails. `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Name

The full name of the user. `Required`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### UserId

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  


## Reference Details

### Person

The person from within the system, which is authenticated with this login. null means that this user is not associated with a person record in the database. `Required` `Default(New Guid)` `Filter(multi eq)` `Inherited from Cm_Persons_Table.Person_Id`

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Inherited From_: **Cm_Persons_Table.Person_Id**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Public_Users?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Public_Users?$top=10>

