---
uid: Communities.SocialGroupMembers
---
# Communities.SocialGroupMembers

Represents the membership of a user in a social group. Entity: Cmm_Social_Group_Members (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Communities.SocialGroupMembers.md#Id) | guid |  
| [JoinTimeUtc](Communities.SocialGroupMembers.md#JoinTimeUtc) | datetime | The exact server time (in UTC), when the user joined the group. [Required] [Default(NowUtc)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [SocialGroup](Communities.SocialGroupMembers.md#SocialGroup) | [Communities.SocialGroups](Communities.SocialGroups.md) | The group in which the user participates. [Required] [Filter(multi eq)] [Owner] |
| [User](Communities.SocialGroupMembers.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who is a member of the group. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### JoinTimeUtc

> The exact server time (in UTC), when the user joined the group. [Required] [Default(NowUtc)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  


## Reference Details

### SocialGroup

> The group in which the user participates. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Communities.SocialGroups](Communities.SocialGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> The user, who is a member of the group. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Communities.SocialGroupMembers erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialGroupMembers erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Communities.SocialGroupMembers erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialGroupMembers?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialGroupMembers?$top=10>

