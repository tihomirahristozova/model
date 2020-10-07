# Communities.SocialPosts

User post in a social group. Entity: Cmm_Social_Posts (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Communities.SocialPosts.md#Id) | guid |  
| [CreationTimeUtc](Communities.SocialPosts.md#CreationTimeUtc) | datetime | The exact server time (in UTC), when the post was created. [Required] 
| [LastInteractionTimeUtc](Communities.SocialPosts.md#LastInteractionTimeUtc) | datetime | The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. [Required] 
| [PostText](Communities.SocialPosts.md#PostText) | string | The post contents in clear text. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [SocialGroup](Communities.SocialPosts.md#SocialGroup) | [Communities.SocialGroups](Communities.SocialGroups.md) | The group in which the post is made. [Required] [Filter(multi eq)] |
| [User](Communities.SocialPosts.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who made the post. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CreationTimeUtc

> The exact server time (in UTC), when the post was created. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LastInteractionTimeUtc

> The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. [Required]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PostText

> The post contents in clear text. [Required]

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### SocialGroup

> The group in which the post is made. [Required] [Filter(multi eq)]

_Type_: **[Communities.SocialGroups](Communities.SocialGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> The user, who made the post. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Communities.SocialPosts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialPosts erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Communities.SocialPosts erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialPosts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialPosts?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cmm_Social_Posts?$top=10>

