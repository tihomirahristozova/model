---
uid: Communities.Notifications
---
# Communities.Notifications Entity

**Namespace:** [Communities](Communities.md)  

A single notification of a user. Entity: Cmm_Notifications (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}: {UserId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Communities.Notifications](Communities.Notifications.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Communities.Notifications.md#creationtimeutc) | datetime | The exact server time (in UTC), when the notification was created. `Required` `Default(NowUtc)` `Filter(ge;le)` `ORD` `ReadOnly` 
| [Id](Communities.Notifications.md#id) | guid |  
| [IsRead](Communities.Notifications.md#isread) | boolean | Specifies whether the user has read the notification. If the system changes the notification after first reading, the flag is reset to unread again. `Required` `Default(false)` `Filter(eq)` 
| [NotificationClass](Communities.Notifications.md#notificationclass) | string (64) | The class of the notification from a predefined list of system classes. `Required` `Filter(multi eq)` 
| [RowVersion](Communities.Notifications.md#rowversion) | byte[] __nullable__ |  
| [Subject](Communities.Notifications.md#subject) | string (256) __nullable__ | The short subject of the notification (in the Default Culture of the user). `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [DataObject](Communities.Notifications.md#dataobject) | [ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) (nullable) | The data object about which the notification is created. Null means that the notification is not about any specific data object. `Filter(multi eq)` |
| [User](Communities.Notifications.md#user) | [Users](Systems.Security.Users.md) | The user, who is notified. `Required` `Filter(multi eq)` |


## Attribute Details

### CreationTimeUtc

The exact server time (in UTC), when the notification was created. `Required` `Default(NowUtc)` `Filter(ge;le)` `ORD` `ReadOnly`

_Type_: **datetime**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **True**  
_Default Value_: **CurrentDateTimeUtc**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsRead

Specifies whether the user has read the notification. If the system changes the notification after first reading, the flag is reset to unread again. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### NotificationClass

The class of the notification from a predefined list of system classes. `Required` `Filter(multi eq)`

_Type_: **string (64)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### RowVersion

_Type_: **byte[] __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Subject

The short subject of the notification (in the Default Culture of the user). `Filter(eq;like)`

_Type_: **string (256) __nullable__**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **256**  


## Reference Details

### DataObject

The data object about which the notification is created. Null means that the notification is not about any specific data object. `Filter(multi eq)`

_Type_: **[ExtensibleDataObjects](Systems.Core.ExtensibleDataObjects.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user, who is notified. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Communities.Notifications erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Communities.Notifications erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_Notifications?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_Notifications?$top=10>

