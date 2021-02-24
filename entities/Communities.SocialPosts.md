---
uid: Communities.SocialPosts
---
# Communities.SocialPosts Entity

**Namespace:** [Communities](Communities.md)  

User post in a social group. Entity: Cmm_Social_Posts (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Communities.SocialPosts](Communities.SocialPosts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Communities.SocialPosts.md#creationtimeutc) | datetime | The exact server time (in UTC), when the post was created. [Required] 
| [Id](Communities.SocialPosts.md#id) | guid |  
| [LastInteractionTimeUtc](Communities.SocialPosts.md#lastinteractiontimeutc) | datetime | The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. [Required] 
| [PostText](Communities.SocialPosts.md#posttext) | string | The post contents in clear text. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [SocialGroup](Communities.SocialPosts.md#socialgroup) | [SocialGroups](Communities.SocialGroups.md) | The group in which the post is made. [Required] [Filter(multi eq)] |
| [User](Communities.SocialPosts.md#user) | [Users](Systems.Security.Users.md) | The user, who made the post. [Required] [Filter(multi eq)] |


## Attribute Details

### CreationTimeUtc

The exact server time (in UTC), when the post was created. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LastInteractionTimeUtc

The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PostText

The post contents in clear text. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### SocialGroup

The group in which the post is made. [Required] [Filter(multi eq)]

_Type_: **[SocialGroups](Communities.SocialGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user, who made the post. [Required] [Filter(multi eq)]

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Communities.SocialPosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialPosts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialPosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialPosts?$top=10>

