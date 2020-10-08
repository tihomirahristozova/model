---
uid: Systems.Core.AttributeChangesHistory
---
# Systems.Core.AttributeChangesHistory

Each entry represents an entity attribute change with previous and new value. Entity: Sys_Attribute_Changes_History_View

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AttributeName](Systems.Core.AttributeChangesHistory.md#attributename) | string |  
| [EntityItemId](Systems.Core.AttributeChangesHistory.md#entityitemid) | guid | The id of the actual changed object, described by this change. [Required] [Filter(multi eq)] 
| [NewValue](Systems.Core.AttributeChangesHistory.md#newvalue) | string (nullable) | The new value. [Filter(eq;like)] 
| [PreviousValue](Systems.Core.AttributeChangesHistory.md#previousvalue) | string | The previous value. [Required] [Filter(eq)] 
| [RepositoryName](Systems.Core.AttributeChangesHistory.md#repositoryname) | string | The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. [Required] [Filter(multi eq;like)] 
| [TimeUtc](Systems.Core.AttributeChangesHistory.md#timeutc) | datetime | Date and time (in Utc) when the changeset was processed by the server. [Required] [Default(NowUtc)] [Filter(eq;ge;le)] [ORD] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [User](Systems.Core.AttributeChangesHistory.md#user) | [Systems.Security.Users](Systems.Security.Users.md) (nullable) | The user which initiated the change. null when it is unknown. [Filter(multi eq)] |


## Attribute Details

### AttributeName

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### EntityItemId

> The id of the actual changed object, described by this change. [Required] [Filter(multi eq)]

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  

### NewValue

> The new value. [Filter(eq;like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### PreviousValue

> The previous value. [Required] [Filter(eq)]

_Type_: **string**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### RepositoryName

> The repository of the actual changed object, described by this change. This is different than the aggregate root, which is pointed by Root Object. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### TimeUtc

> Date and time (in Utc) when the changeset was processed by the server. [Required] [Default(NowUtc)] [Filter(eq;ge;le)] [ORD]

_Type_: **datetime**  
_Supported Filters_: **Equals, GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDateTimeUtc**  


## Reference Details

### User

> The user which initiated the change. null when it is unknown. [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Systems.Core.AttributeChangesHistory erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Systems.Core.AttributeChangesHistory erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Systems.Core.AttributeChangesHistory erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Systems_Core_AttributeChangesHistory?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Systems_Core_AttributeChangesHistory?$top=10>

