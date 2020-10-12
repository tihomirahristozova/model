---
uid: Systems.Core.ObjectVersions
---
# Systems.Core.ObjectVersions Entity

Contains history of saved version of the managed objects. Entity: Sys_Object_Versions

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.ObjectVersions.md#id) | guid |  
| [ObjectContents](Systems.Core.ObjectVersions.md#objectcontents) | byte[] | The compressed contents of the object. [Required] 
| [ServerVersion](Systems.Core.ObjectVersions.md#serverversion) | string (nullable) | The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). null means the version is unknown. 
| [Version](Systems.Core.ObjectVersions.md#version) | int32 | The version number of the version, stored in the current row, starting from 1. [Required] [Filter(multi eq;ge;le)] 
| [VersionTime](Systems.Core.ObjectVersions.md#versiontime) | datetime | The timestamp when the version was saved. [Required] [Filter(ge;le)] 
| [VersionType](Systems.Core.ObjectVersions.md#versiontype) | [VersionType](Systems.Core.ObjectVersions.md#versiontype) | Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Object](Systems.Core.ObjectVersions.md#object) | [ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) | The object, for which a version is stored. [Required] [Filter(multi eq)] [Owner] |
| [User](Systems.Core.ObjectVersions.md#user) | [Users](Systems.Security.Users.md) | The user, which saved the version. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectContents

The compressed contents of the object. [Required]

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ServerVersion

The version of the EnterpriseOne server, which created the version. The version should be in the form (9.9.9.9). null means the version is unknown.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Version

The version number of the version, stored in the current row, starting from 1. [Required] [Filter(multi eq;ge;le)]

_Type_: **int32**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### VersionTime

The timestamp when the version was saved. [Required] [Filter(ge;le)]

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### VersionType

Specifies the action, which occurred on the actual object, referred by the system object.  'C' means that with this version the object was created. 'U' means that this is an update to an existing object. [Required]

_Type_: **[VersionType](Systems.Core.ObjectVersions.md#versiontype)**  
Allowed values for the [VersionType](Systems.Core.ObjectVersions.md#versiontype) data attribute  
_Allowed Values (Systems.Core.ObjectVersionsRepository.VersionType Enum Members)_  

| Value | Description |
| ---- | --- |
| Create | Create value. Stored as 'C'. <br /> _Database Value:_ 'C' <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'Create' |
| Update | Update value. Stored as 'U'. <br /> _Database Value:_ 'U' <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'Update' |

_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Object

The object, for which a version is stored. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user, which saved the version. [Required] [Filter(multi eq)]

_Type_: **[Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Core.ObjectVersions erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ObjectVersions erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ObjectVersions?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ObjectVersions?$top=10>

