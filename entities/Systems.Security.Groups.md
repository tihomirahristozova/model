# Systems.Security.Groups

Groups of users. Used for providing group access to secured data. Entity: Sec_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Security.Groups.md#Id) | guid |  
| [EditPeriodDays](Systems.Security.Groups.md#EditPeriodDays) | int32 (nullable) | The number of days before which the documents can not be corrected, released or voided. 
| [Name](Systems.Security.Groups.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | The name of this Group. [Required] [Filter(like)] [ORD] 
| [GroupType](Systems.Security.Groups.md#GroupType) | [Systems.Security.GroupsRepository.GroupType](Systems.Security.Groups.md#GroupType) | Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody. [Required] [Default("G")] [ReadOnly] 
| [Notes](Systems.Security.Groups.md#Notes) | string (nullable) | Notes for this Group. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [GroupForUser](Systems.Security.Groups.md#GroupForUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | When Group_Type=U, contains the user for which the group is defined, null otherwise. [Filter(multi eq)] [ReadOnly] |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| AccessKeys | [Systems.Security.GroupAccessKeys](Systems.Security.GroupAccessKeys.md) | List of [GroupAccessKey](Systems.Security.GroupAccessKeys.md) child objects, based on the [Systems.Security.GroupAccessKey.Group](Systems.Security.GroupAccessKeys.md#Group) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### EditPeriodDays

> The number of days before which the documents can not be corrected, released or voided.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Name

> The name of this Group. [Required] [Filter(like)] [ORD]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### GroupType

> Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody. [Required] [Default("G")] [ReadOnly]

_Type_: **[Systems.Security.GroupsRepository.GroupType](Systems.Security.Groups.md#GroupType)**  
Allowed values for the [GroupType](Systems.Security.Groups.md#GroupType) data attribute  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| NormalUserDefinableGroup | NormalUserDefinableGroup value. Stored as 'G'. <br /> _Database Value:_ 'G' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NormalUserDefinableGroup' |
| SystemGroupForOneUser | SystemGroupForOneUser value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SystemGroupForOneUser' |
| Administrators | Administrators value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Administrators' |
| Everybody | Everybody value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Everybody' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **NormalUserDefinableGroup**  

### Notes

> Notes for this Group.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### GroupForUser

> When Group_Type=U, contains the user for which the group is defined, null otherwise. [Filter(multi eq)] [ReadOnly]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Security.Groups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Security.Groups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Security.Groups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_Groups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_Groups?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Sec_Groups?$top=10>

