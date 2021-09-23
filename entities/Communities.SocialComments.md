---
uid: Communities.SocialComments
---
# Communities.SocialComments Entity

**Namespace:** [Communities](Communities.md)  

User comment to any object in the system. Entity: Cmm_Social_Comments (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Communities.SocialComments](Communities.SocialComments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CommentText](Communities.SocialComments.md#commenttext) | string (max) | The comment contents in clear text. `Required` 
| [CreationTimeUtc](Communities.SocialComments.md#creationtimeutc) | datetime | The exact server time (in UTC), when the comment was created. `Required` `ORD` 
| [Id](Communities.SocialComments.md#id) | guid |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataObject](Communities.SocialComments.md#dataobject) | [ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | The root data object (post, marketplace product, document, etc), for which the comment is made. `Required` `Filter(multi eq)` |
| [ReplyToComment](Communities.SocialComments.md#replytocomment) | [SocialComments](Communities.SocialComments.md) (nullable) | When not null, means that the comment is a reply to the specified comment. The comment and the reply should be for the same data object. `Filter(multi eq)` |
| [User](Communities.SocialComments.md#user) | [Users](Systems.Security.Users.md) | The user, who made the comment. `Required` `Filter(multi eq)` |


## Attribute Details

### CommentText

The comment contents in clear text. `Required`

_Type_: **string (max)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### CreationTimeUtc

The exact server time (in UTC), when the comment was created. `Required` `ORD`

_Type_: **datetime**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  


## Reference Details

### DataObject

The root data object (post, marketplace product, document, etc), for which the comment is made. `Required` `Filter(multi eq)`

_Type_: **[ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ReplyToComment

When not null, means that the comment is a reply to the specified comment. The comment and the reply should be for the same data object. `Filter(multi eq)`

_Type_: **[SocialComments](Communities.SocialComments.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user, who made the comment. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Communities.SocialComments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Communities.SocialComments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialComments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialComments?$top=10>

