# Communities.SocialReactionsSummary

Summary with the social reactions per comment and dataobject. Entity: Cmm_Social_Reactions_Summary_Indexed_View

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Cnt](Communities.SocialReactionsSummary.md#Cnt) | int64 |  
| [ReactionType](Communities.SocialReactionsSummary.md#ReactionType) | [Communities.SocialReactionsSummaryRepository.ReactionType](Communities.SocialReactionsSummary.md#ReactionType) | The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataObject](Communities.SocialReactionsSummary.md#DataObject) | [Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | . [Required] [Default(New Guid)] [Filter(multi eq)] |
| [SocialComment](Communities.SocialReactionsSummary.md#SocialComment) | [Communities.SocialComments](Communities.SocialComments.md) |  |


## Attribute Details

### Cnt

_Type_: **int64**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ReactionType

> The type of the reaction. LIK = Like; LOV = Love; HAH = Haha; WOW = Wow; SAD = Sad; ANG = Angry. [Required]

_Type_: **[Communities.SocialReactionsSummaryRepository.ReactionType](Communities.SocialReactionsSummary.md#ReactionType)**  
Allowed values for the [ReactionType](Communities.SocialReactionsSummary.md#ReactionType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| Like | Compare by mask. Use * (asterisk) as wildcard char.. Stored as 'LIK'. <br /> _Database Value:_ 'LIK' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Like' |
| Love | Love value. Stored as 'LOV'. <br /> _Database Value:_ 'LOV' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Love' |
| Haha | Haha value. Stored as 'HAH'. <br /> _Database Value:_ 'HAH' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Haha' |
| Wow | Wow value. Stored as 'WOW'. <br /> _Database Value:_ 'WOW' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Wow' |
| Sad | Sad value. Stored as 'SAD'. <br /> _Database Value:_ 'SAD' <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'Sad' |
| Angry | Angry value. Stored as 'ANG'. <br /> _Database Value:_ 'ANG' <br /> _Model Value:_ 5 <br /> _Domain API Value:_ 'Angry' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### DataObject

> . [Required] [Default(New Guid)] [Filter(multi eq)]

_Type_: **[Systems.Core.ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### SocialComment

_Type_: **[Communities.SocialComments](Communities.SocialComments.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  



## Business Rules

[!list erp.entity=Communities.SocialReactionsSummary erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.SocialReactionsSummary erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Communities.SocialReactionsSummary erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_SocialReactionsSummary?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_SocialReactionsSummary?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Cmm_Social_Reactions_Summary_Indexed_View?$top=10>

