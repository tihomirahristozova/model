---
uid: General.Contacts.PartyPictures
---
# General.Contacts.PartyPictures

Party pictures - photos, logos, etc. Entity: Gen_Party_Pictures

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Comments](General.Contacts.PartyPictures.md#comments) | string (nullable) | Notes for this party picture. 
| [Id](General.Contacts.PartyPictures.md#id) | guid |  
| [IsDefault](General.Contacts.PartyPictures.md#isdefault) | boolean | True=This is the default picture for the party; false=otherwise. [Required] [Default(false)] [Filter(eq)] 
| [IsLogo](General.Contacts.PartyPictures.md#islogo) | boolean | If checked specifies that this picture is used to visualize the logo of this party in the system. [Required] [Default(false)] [Filter(eq)] 
| [Picture](General.Contacts.PartyPictures.md#picture) | byte[] (nullable) | The actual party picture data. Can be null if we insert only some comments. 
| [PictureNo](General.Contacts.PartyPictures.md#pictureno) | int32 | Unique picture number within the party. Also used for sorting. [Required] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Party](General.Contacts.PartyPictures.md#party) | [Parties](General.Contacts.Parties.md) | The [Party](General.Contacts.PartyPictures.md#party) to which this PartyPicture belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Comments

> Notes for this party picture.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDefault

> True=This is the default picture for the party; false=otherwise. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

_Front-End Recalc Expressions:_  
`( obj.Party.Pictures.Take( 1).Count( ) == 0)`
### IsLogo

> If checked specifies that this picture is used to visualize the logo of this party in the system. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Picture

> The actual party picture data. Can be null if we insert only some comments.

_Type_: **byte[] (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PictureNo

> Unique picture number within the party. Also used for sorting. [Required] [Filter(eq)]

_Type_: **int32**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

_Back-End Default Expression:_  
`( obj.Party.Pictures.Select( c => c.PictureNo).DefaultIfEmpty( 0).Max( ) + 10)`

_Front-End Recalc Expressions:_  
`( obj.Party.Pictures.Select( c => c.PictureNo).DefaultIfEmpty( 0).Max( ) + 10)`

## Reference Details

### Party

> The [Party](General.Contacts.PartyPictures.md#party) to which this PartyPicture belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.PartyPictures erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.PartyPictures erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.PartyPictures erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyPictures?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyPictures?$top=10>

