---
uid: Systems.Security.Groups
---
# Systems.Security.Groups Entity

**Namespace:** [Systems.Security](Systems.Security.md)  

Groups of users. Used for providing group access to secured data. Entity: Sec_Groups

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Security.Groups](Systems.Security.Groups.md)  
  * [Systems.Security.GroupAccessKeys](Systems.Security.GroupAccessKeys.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EditPeriodDays](Systems.Security.Groups.md#editperioddays) | int32 __nullable__ | The number of days before which the documents can not be corrected, released or voided. 
| [GroupType](Systems.Security.Groups.md#grouptype) | [GroupType](Systems.Security.Groups.md#grouptype) | Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody. `Required` `Default("G")` `ReadOnly` 
| [Id](Systems.Security.Groups.md#id) | guid |  
| [Name](Systems.Security.Groups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | The name of this Group. `Required` `Filter(like)` `ORD` 
| [Notes](Systems.Security.Groups.md#notes) | string (254) __nullable__ | Notes for this Group. 
| [RowVersion](Systems.Security.Groups.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [GroupForUser](Systems.Security.Groups.md#groupforuser) | [Users](Systems.Security.Users.md) (nullable) | When Group_Type=U, contains the user for which the group is defined, null otherwise. `Filter(multi eq)` `ReadOnly` |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| AccessKeys | [GroupAccessKeys](Systems.Security.GroupAccessKeys.md) | List of `GroupAccessKey`(Systems.Security.GroupAccessKeys.md) child objects, based on the `Systems.Security.GroupAccessKey.Group`(Systems.Security.GroupAccessKeys.md#group) back reference 


## Attribute Details

### EditPeriodDays

The number of days before which the documents can not be corrected, released or voided.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### GroupType

Group type. G=Normal user-definable group; U=System group for 1 user; A=Admin; E=Everybody. `Required` `Default("G")` `ReadOnly`

_Type_: **[GroupType](Systems.Security.Groups.md#grouptype)**  
Allowed values for the `GroupType`(Systems.Security.Groups.md#grouptype) data attribute  
_Allowed Values (Systems.Security.GroupsRepository.GroupType Enum Members)_  

| Value | Description |
| ---- | --- |
| NormalUserDefinableGroup | NormalUserDefinableGroup value. Stored as 'G'. <br /> _Database Value:_ 'G' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'NormalUserDefinableGroup' |
| SystemGroupForOneUser | SystemGroupForOneUser value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'SystemGroupForOneUser' |
| Administrators | Administrators value. Stored as 'A'. <br /> _Database Value:_ 'A' <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'Administrators' |
| Everybody | Everybody value. Stored as 'E'. <br /> _Database Value:_ 'E' <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'Everybody' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **NormalUserDefinableGroup**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

The name of this Group. `Required` `Filter(like)` `ORD`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Like**  
_Supports Order By_: **True**  

### Notes

Notes for this Group.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### GroupForUser

When Group_Type=U, contains the user for which the group is defined, null otherwise. `Filter(multi eq)` `ReadOnly`

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Systems.Security.Groups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Systems.Security.Groups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Security_Groups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Security_Groups?$top=10>

