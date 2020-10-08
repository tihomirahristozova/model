---
uid: Communities.SocialReactions
---
# Communities.SocialReactions

Reaction of a user to any social comment to an object of the system. Entity: Cmm_Social_Reactions (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Communities.SocialReactions.md#Id) | guid |  
| [CreationTimeUtc](Communities.SocialReactions.md#CreationTimeUtc) | datetime | The exact server time (in UTC), when the reaction was created. [Required] [Default(NowUtc)] 
| [ReactionType](Communities.SocialReactions.md#ReactionType) | [Communities.SocialReactionsRepository.ReactionType](Communities.SocialReactions.md#ReactionType) | The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry. [Required] [Filter(multi eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataObject](Communities.SocialReactions.md#DataObject) | [Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | The root data object (post, marketplace product, document, etc), for which the reaction is. [Required] [Filter(multi eq)] |
| [SocialComment](Communities.SocialReactions.md#SocialComment) | [Communities.SocialComments](Communities.SocialComments.md) (nullable) | When not null, specifies that the reaction is for the specified comment within the data object. [Filter(multi eq)] |
| [User](Communities.SocialReactions.md#User) | [Systems.Security.Users](Systems.Security.Users.md) | The user, who reacted. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CreationTimeUtc

> The exact server time (in UTC), when the reaction was created. [Required] [Default(NowUtc)]

_Type_: **datetime**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTimeUtc**  

### ReactionType

> The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry. [Required] [Filter(multi eq)]

_Type_: **[Communities.SocialReactionsRepository.ReactionType](Communities.SocialReactions.md#ReactionType)**  
Allowed values for the [ReactionType](Communities.SocialReactions.md#ReactionType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Like | Compare by mask. Use * (asterisk) as wildcard char.. Stored as 'LIK'. <br /> _Database Value:_ 'LIK' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Like' |
| Love | Love value. Stored as 'LOV'. <br /> _Database Value:_ 'LOV' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Love' |
| Haha | Haha value. Stored as 'HAH'. <br /> _Database Value:_ 'HAH' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Haha' |
| Wow | Wow value. Stored as 'WOW'. <br /> _Database Value:_ 'WOW' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Wow' |
| Sad | Sad value. Stored as 'SAD'. <br /> _Database Value:_ 'SAD' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Sad' |
| Angry | Angry value. Stored as 'ANG'. <br /> _Database Value:_ 'ANG' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Angry' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### DataObject

> The root data object (post, marketplace product, document, etc), for which the reaction is. [Required] [Filter(multi eq)]

_Type_: **[Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### SocialComment

> When not null, specifies that the reaction is for the specified comment within the data object. [Filter(multi eq)]

_Type_: **[Communities.SocialComments](Communities.SocialComments.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### User

> The user, who reacted. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Communities.SocialReactions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialReactions erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Communities.SocialReactions erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialReactions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialReactions?$top=10>

