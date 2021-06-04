---
uid: Systems.Security.UserGroups
---
# Systems.Security.UserGroups Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Contains the user group members. Entity: Sec_User_Groups

## Default Visualization
Default Display Text Format:  
_{User.PhoneNumber}: {User.Name:T}_  
Default Search Member:  
_User.PhoneNumber_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Systems.Security.Users](Systems.Security.Users.md)  
Aggregate Root:  
[Systems.Security.Users](Systems.Security.Users.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.UserGroups.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Group](Systems.Security.UserGroups.md#group) | [Groups](Systems.Security.Groups.md) | The group, in which the user is included. `Required` `Filter(multi eq)` |
| [User](Systems.Security.UserGroups.md#user) | [Users](Systems.Security.Users.md) | The `User`(Systems.Security.UserGroups.md#user) to which this UserGroup belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### Group

The group, in which the user is included. `Required` `Filter(multi eq)`

_Type_: **[Groups](Systems.Security.Groups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The `User`(Systems.Security.UserGroups.md#user) to which this UserGroup belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Users](Systems.Security.Users.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  



## Business Rules

[!list erp.entity=Systems.Security.UserGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.UserGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_UserGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_UserGroups?$top=10>

