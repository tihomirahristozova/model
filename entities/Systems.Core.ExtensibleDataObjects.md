---
uid: Systems.Core.ExtensibleDataObjects
---
# Systems.Core.ExtensibleDataObjects

Extends data in other tables with attached files, custom properties, etc. Each row is an object, bound to exactly one row in the primary table. Each object can be bound to a row in a different primary table, specified in Entity_Type. Entity: Sys_Objects

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Systems.Core.ExtensibleDataObjects.md#Id) | guid |  
| [CreationTimeUtc](Systems.Core.ExtensibleDataObjects.md#CreationTimeUtc) | datetime (nullable) | The exact server time (in UTC) when the object represented by this system object was created. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1.100.0) 
| [EntityItemId](Systems.Core.ExtensibleDataObjects.md#EntityItemId) | guid | The Id of the primary row to which the object is bound. [Required] [Filter(multi eq)] 
| [EntityType](Systems.Core.ExtensibleDataObjects.md#EntityType) | string | The entity type of the row to which the object is bound. [Required] [Default(" ")] [Filter(eq)] [ORD] 
| [IsDeleted](Systems.Core.ExtensibleDataObjects.md#IsDeleted) | boolean | Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes. [Required] [Default(false)] [Filter(eq)] (Introduced in version 19.1.100.0) 
| [LastUpdateTimeUtc](Systems.Core.ExtensibleDataObjects.md#LastUpdateTimeUtc) | datetime (nullable) | The exact server time (in UTC) of the last modification of the object represented by this system object. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1.100.0) 
| [LatestVersion](Systems.Core.ExtensibleDataObjects.md#LatestVersion) | int32 | The latest saved version of the object. Starts from 1 and increments with 1 for each new version. [Required] [Default(1)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationUser](Systems.Core.ExtensibleDataObjects.md#CreationUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user, who created the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1.100.0) |
| [LastUpdateUser](Systems.Core.ExtensibleDataObjects.md#LastUpdateUser) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user, who made the last modification of the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1.100.0) |

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Files | [Systems.Core.ObjectFiles](Systems.Core.ObjectFiles.md) | List of [ObjectFile](Systems.Core.ObjectFiles.md) child objects, based on the [Systems.Core.ObjectFile.Object](Systems.Core.ObjectFiles.md#Object) back reference 
| Versions | [Systems.Core.ObjectVersions](Systems.Core.ObjectVersions.md) | List of [ObjectVersion](Systems.Core.ObjectVersions.md) child objects, based on the [Systems.Core.ObjectVersion.Object](Systems.Core.ObjectVersions.md#Object) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### CreationTimeUtc

> The exact server time (in UTC) when the object represented by this system object was created. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1.100.0)

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### EntityItemId

> The Id of the primary row to which the object is bound. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### EntityType

> The entity type of the row to which the object is bound. [Required] [Default(" ")] [Filter(eq)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **True**  
_Default Value_: ** **  

### IsDeleted

> Specifies whether the object represented by this system object is deleted. After deletion of the original object, the system object remains in the system, but can be purged later by some cleanup processes. [Required] [Default(false)] [Filter(eq)] (Introduced in version 19.1.100.0)

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### LastUpdateTimeUtc

> The exact server time (in UTC) of the last modification of the object represented by this system object. null means that it is unknown. [Filter(ge;le)] (Introduced in version 19.1.100.0)

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### LatestVersion

> The latest saved version of the object. Starts from 1 and increments with 1 for each new version. [Required] [Default(1)]

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **1**  


## Reference Details

### CreationUser

> The user, who created the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### LastUpdateUser

> The user, who made the last modification of the object represented by this system object . null means that it is unknown. [Filter(multi eq)] (Introduced in version 19.1.100.0)

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Systems.Core.ExtensibleDataObjects erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.ExtensibleDataObjects erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.ExtensibleDataObjects erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_ExtensibleDataObjects?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_ExtensibleDataObjects?$top=10>

