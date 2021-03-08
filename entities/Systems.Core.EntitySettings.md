---
uid: Systems.Core.EntitySettings
---
# Systems.Core.EntitySettings Entity

**Namespace:** [Systems.Core](Systems.Core.md)  

Contains entities, which have secured access. Entity: Sys_Entities

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Systems.Core.EntitySettings](Systems.Core.EntitySettings.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.EntitySettings.md#id) | guid |  
| [LogCreate](Systems.Core.EntitySettings.md#logcreate) | boolean | Specifies whether to log every insert for this entity. `Required` `Default(false)` `Introduced in version 18.2` 
| [LogDelete](Systems.Core.EntitySettings.md#logdelete) | boolean | Specifies whether to log every delete for this entity. `Required` `Default(false)` `Introduced in version 18.2` 
| [LogReadById](Systems.Core.EntitySettings.md#logreadbyid) | boolean | Specifies whether to log every load by Id for this entity. `Required` `Default(false)` `Introduced in version 18.2` 
| [LogReadMany](Systems.Core.EntitySettings.md#logreadmany) | boolean | Specifies whether to log every load of many records for this entity. `Required` `Default(false)` `Introduced in version 18.2` 
| [LogUpdate](Systems.Core.EntitySettings.md#logupdate) | boolean | Specifies whether to log every update for this entity. `Required` `Default(false)` `Introduced in version 18.2` 
| [Name](Systems.Core.EntitySettings.md#name) | string | The system name of the entity, which is being secured. `Required` `Filter(eq;like)` `ORD` 
| [TrackChangesLevel](Systems.Core.EntitySettings.md#trackchangeslevel) | [TrackChangesLevel](Systems.Core.EntitySettings.md#trackchangeslevel) | The track changes level for the entity. `Required` `Default(0)` `Filter(multi eq)` `Introduced in version 19.1` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [AccessKey](Systems.Core.EntitySettings.md#accesskey) | [AccessKeys](Systems.Security.AccessKeys.md) (nullable) | The access key, required to access the secured entity. `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LogCreate

Specifies whether to log every insert for this entity. `Required` `Default(false)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogDelete

Specifies whether to log every delete for this entity. `Required` `Default(false)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogReadById

Specifies whether to log every load by Id for this entity. `Required` `Default(false)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogReadMany

Specifies whether to log every load of many records for this entity. `Required` `Default(false)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LogUpdate

Specifies whether to log every update for this entity. `Required` `Default(false)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Name

The system name of the entity, which is being secured. `Required` `Filter(eq;like)` `ORD`

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### TrackChangesLevel

The track changes level for the entity. `Required` `Default(0)` `Filter(multi eq)` `Introduced in version 19.1`

_Type_: **[TrackChangesLevel](Systems.Core.EntitySettings.md#trackchangeslevel)**  
Represents the different levels of tracking changes for a specific entity.  
_Allowed Values (Systems.Core.TrackChangesLevel Enum Members)_  

| Value | Description |
| ---- | --- |
| DoNotTrackChanges | The do not track changes for this entity. <br /> _Database Value:_ 0 <br /> _Model Value:_ 0 <br /> _Domain API Value:_ 'DoNotTrackChanges' |
| TrackLastChangesOnly | The track last changes only: creation time, creation user, last update time, last update user. <br /> _Database Value:_ 1 <br /> _Model Value:_ 1 <br /> _Domain API Value:_ 'TrackLastChangesOnly' |
| TrackObjectChanges | Only object changes are tracked. The changed attributes are not tracked. <br /> _Database Value:_ 2 <br /> _Model Value:_ 2 <br /> _Domain API Value:_ 'TrackObjectChanges' |
| TrackObjectAnd<br />AttributeChanges | Object and attribute changes are tracked excluding BLOB attributes. <br /> _Database Value:_ 3 <br /> _Model Value:_ 3 <br /> _Domain API Value:_ 'TrackObjectAnd<br />AttributeChanges' |
| TrackObjectAttribute<br />AndBlobChanges | Object and attribute changes are tracked including BLOB attributes. <br /> _Database Value:_ 4 <br /> _Model Value:_ 4 <br /> _Domain API Value:_ 'TrackObjectAttribute<br />AndBlobChanges' |

_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **0**  


## Reference Details

### AccessKey

The access key, required to access the secured entity. `Filter(multi eq)`

_Type_: **[AccessKeys](Systems.Security.AccessKeys.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Core.EntitySettings erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.EntitySettings erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_EntitySettings?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_EntitySettings?$top=10>

