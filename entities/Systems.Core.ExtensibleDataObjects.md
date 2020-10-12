---
uid: Systems.Core.ExtensibleDataObjects
---
# Systems.Core.ExtensibleDataObjects Entity

Extends data in other tables with attached files, custom properties, etc. Each row is an object, bound to exactly one row in the primary table. Each object can be bound to a row in a different primary table, specified in Entity_Type. Entity: Sys_Objects

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Systems.Core.ExtensibleDataObjects.md#creationtimeutc) | datetime (nullable) | The exact server time (in UTC) when the object represented by this system object was created. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1) 
| [EntityItemId](Systems.Core.ExtensibleDataObjects.md#entityitemid) | guid | The Id of the primary row to which the object is bound. [Required] [Filter(multi eq)] 
| [EntityType](Systems.Core.ExtensibleDataObjects.md#entitytype) | string | The entity type of the row to which the object is bound. [Required] [Default(" ")] [Filter(eq)] [ORD] 
| [Id](Systems.Core.ExtensibleDataObjects.md#id) | guid |  
| [IsDeleted](Systems.Core.ExtensibleDataObjects.md#isdeleted) | boolean | Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes. [Required] [Default(false)] [Filter(eq)] (Introduced in version 19.1) 
| [LastUpdateTimeUtc](Systems.Core.ExtensibleDataObjects.md#lastupdatetimeutc) | datetime (nullable) | The exact server time (in UTC) of the last modification of the object represented by this system object. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1) 
| [LatestVersion](Systems.Core.ExtensibleDataObjects.md#latestversion) | int32 | The latest saved version of the object. Starts from 1 and increments with 1 for each new version. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Systems.Core.ExtensibleDataObjects.md#creationuser) | [Users](Systems.Security.Users.md) (nullable) | The user, who created the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1) |
| [LastUpdateUser](Systems.Core.ExtensibleDataObjects.md#lastupdateuser) | [Users](Systems.Security.Users.md) (nullable) | The user, who made the last modification of the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1) |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Files | [ObjectFiles](Systems.Core.ObjectFiles.md) | List of [ObjectFile](Systems.Core.ObjectFiles.md) child objects, based on the [Systems.Core.ObjectFile.Object](Systems.Core.ObjectFiles.md#object) back reference 
| Versions | [ObjectVersions](Systems.Core.ObjectVersions.md) | List of [ObjectVersion](Systems.Core.ObjectVersions.md) child objects, based on the [Systems.Core.ObjectVersion.Object](Systems.Core.ObjectVersions.md#object) back reference 


## Attribute Details

### CreationTimeUtc

The exact server time (in UTC) when the object represented by this system object was created. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1)

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### EntityItemId

The Id of the primary row to which the object is bound. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### EntityType

The entity type of the row to which the object is bound. [Required] [Default(" ")] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Default Value_: ** **  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDeleted

Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes. [Required] [Default(false)] [Filter(eq)] (Introduced in version 19.1)

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LastUpdateTimeUtc

The exact server time (in UTC) of the last modification of the object represented by this system object. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1)

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### LatestVersion

The latest saved version of the object. Starts from 1 and increments with 1 for each new version. [Required] [Default(1)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### CreationUser

The user, who created the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1)

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### LastUpdateUser

The user, who made the last modification of the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1)

_Type_: **[Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Core.ExtensibleDataObjects erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ExtensibleDataObjects erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ExtensibleDataObjects?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ExtensibleDataObjects?$top=10>

