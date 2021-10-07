---
uid: Systems.Security.UserAccessKeys
---
# Systems.Security.UserAccessKeys Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Obsolete. Not used. Entity: Sec_User_Access_Keys

## Default Visualization
Default Display Text Format:  
_{User.Name:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Security.Users](Systems.Security.Users.md)  
Aggregate Root:  
[Systems.Security.Users](Systems.Security.Users.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CanDelete](Systems.Security.UserAccessKeys.md#candelete) | boolean | Obsolete. Not used. `Required` 
| [CanUpdate](Systems.Security.UserAccessKeys.md#canupdate) | boolean | Obsolete. Not used. `Required` 
| [Id](Systems.Security.UserAccessKeys.md#id) | guid |  
| [Permission1](Systems.Security.UserAccessKeys.md#permission1) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission10](Systems.Security.UserAccessKeys.md#permission10) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission2](Systems.Security.UserAccessKeys.md#permission2) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission3](Systems.Security.UserAccessKeys.md#permission3) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission4](Systems.Security.UserAccessKeys.md#permission4) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission5](Systems.Security.UserAccessKeys.md#permission5) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission6](Systems.Security.UserAccessKeys.md#permission6) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission7](Systems.Security.UserAccessKeys.md#permission7) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission8](Systems.Security.UserAccessKeys.md#permission8) | boolean | Obsolete. Not used. `Required` `Default(false)` 
| [Permission9](Systems.Security.UserAccessKeys.md#permission9) | boolean | Obsolete. Not used. `Required` `Default(false)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Security.UserAccessKeys.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) | The access key, containing the user permissions for this UserAccessKey. Null means that all users have unlimited permissions. `Required` `Filter(multi eq)` |
| [User](Systems.Security.UserAccessKeys.md#user) | [Users](Systems.Security.Users.md) | Obsolete. Not used. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### CanDelete

Obsolete. Not used. `Required`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CanUpdate

Obsolete. Not used. `Required`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Permission1

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission10

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission2

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission3

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission4

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission5

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission6

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission7

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission8

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Permission9

Obsolete. Not used. `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### AccessKey

The access key, containing the user permissions for this UserAccessKey. Null means that all users have unlimited permissions. `Required` `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

Obsolete. Not used. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Security.UserAccessKeys erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.UserAccessKeys erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_UserAccessKeys?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_UserAccessKeys?$top=10>

