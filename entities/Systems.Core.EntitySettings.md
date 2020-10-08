---
uid: Systems.Core.EntitySettings
---
# Systems.Core.EntitySettings

Contains entities, which have secured access. Entity: Sys_Entities

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.EntitySettings.md#Id) | guid |  
| [Name](Systems.Core.EntitySettings.md#Name) | string | The system name of the entity, which is being secured. [Required] [Filter(eq;like)] [ORD] 
| [LogCreate](Systems.Core.EntitySettings.md#LogCreate) | boolean | Specifies whether to log every insert for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0) 
| [LogDelete](Systems.Core.EntitySettings.md#LogDelete) | boolean | Specifies whether to log every delete for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0) 
| [LogReadById](Systems.Core.EntitySettings.md#LogReadById) | boolean | Specifies whether to log every load by Id for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0) 
| [LogReadMany](Systems.Core.EntitySettings.md#LogReadMany) | boolean | Specifies whether to log every load of many records for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0) 
| [LogUpdate](Systems.Core.EntitySettings.md#LogUpdate) | boolean | Specifies whether to log every update for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0) 
| [TrackChangesLevel](Systems.Core.EntitySettings.md#TrackChangesLevel) | [Systems.Core.TrackChangesLevel](Systems.Core.EntitySettings.md#TrackChangesLevel) | The track changes level for the entity. [Required] [Default(0)] [Filter(multi eq)] (Introduced in version 19.1.100.0) 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Core.EntitySettings.md#AccessKey) | [Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, required to access the secured entity. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Name

> The system name of the entity, which is being secured. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### LogCreate

> Specifies whether to log every insert for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogDelete

> Specifies whether to log every delete for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogReadById

> Specifies whether to log every load by Id for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogReadMany

> Specifies whether to log every load of many records for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogUpdate

> Specifies whether to log every update for this entity. [Required] [Default(false)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### TrackChangesLevel

> The track changes level for the entity. [Required] [Default(0)] [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Systems.Core.TrackChangesLevel](Systems.Core.EntitySettings.md#TrackChangesLevel)**  
Represents the different levels of tracking changes for a specific entity.  
_Allowed Values (Enum Members)_  

| Value | Description |
| ---- | --- |
| DoNotTrackChanges | The do not track changes for this entity. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'DoNotTrackChanges' |
| TrackLastChangesOnly | The track last changes only: creation time, creation user, last update time, last update user. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'TrackLastChangesOnly' |
| TrackObjectChanges | Only object changes are tracked. The changed attributes are not tracked. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'TrackObjectChanges' |
| TrackObjectAndAttributeChanges | Object and attribute changes are tracked excluding BLOB attributes. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'TrackObjectAndAttributeChanges' |
| TrackObjectAttributeAndBlobChanges | Object and attribute changes are tracked including BLOB attributes. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'TrackObjectAttributeAndBlobChanges' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### AccessKey

> The access key, required to access the secured entity. [Filter(multi eq)]

_Type_: **[Systems.Security.AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.EntitySettings erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.EntitySettings erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.EntitySettings erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_EntitySettings?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_EntitySettings?$top=10>

