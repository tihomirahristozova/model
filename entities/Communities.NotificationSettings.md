---
uid: Communities.NotificationSettings
---
# Communities.NotificationSettings Entity

**Namespace:** [Communities](Communities.md)  

User notification settings for the different notification classes. Entity: Cmm_Notification_Settings (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}: {ObjectVersion}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Communities.NotificationSettings](Communities.NotificationSettings.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Communities.NotificationSettings.md#id) | guid |  
| [NotificationClass](Communities.NotificationSettings.md#notificationclass) | string (64) __nullable__ | The class of the notification, for which the user is specifying settings. When null, the setting is applied to all notification classes. `Filter(multi eq)` 
| [ObjectVersion](Communities.NotificationSettings.md#objectversion) | int32 |  
| [ReceiveMail](Communities.NotificationSettings.md#receivemail) | boolean | True if the user should receive mail. `Required` `Default(false)` `Filter(eq)` 
| [ReceiveNotification](Communities.NotificationSettings.md#receivenotification) | boolean | True if the user should receive internal notification. `Required` `Default(true)` `Filter(eq)` 
| [ReceiveSms](Communities.NotificationSettings.md#receivesms) | boolean | True if the user should receive SMS. `Required` `Default(false)` `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [User](Communities.NotificationSettings.md#user) | [Users](Systems.Security.Users.md) | The user for whom the notification setting is about. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### NotificationClass

The class of the notification, for which the user is specifying settings. When null, the setting is applied to all notification classes. `Filter(multi eq)`

_Type_: **string (64) __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **64**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ReceiveMail

True if the user should receive mail. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReceiveNotification

True if the user should receive internal notification. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ReceiveSms

True if the user should receive SMS. `Required` `Default(false)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### User

The user for whom the notification setting is about. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  


## API Methods

Methods that can be invoked in public APIs.

### GetAllowedCustomPropertyValues

Gets the allowed values for the specified custom property for this entity object.              If supported the result is ordered by property value. Some property value sources do not support ordering - in that case the result is not ordered.  
_Return Type_: **Collection Of [CustomPropertyValue](../data-types.md#general.custompropertyvalue)**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **GET**  

**Parameters**  
  * **customPropertyCode**  
    The code of the custom property  
    _Type_: string  

  * **search**  
    The search text - searches by value or description. Can contain wildcard character %.  
    _Type_: string  
     _Optional_: True  
    _Default Value_: null  

  * **exactMatch**  
    If true the search text should be equal to the property value  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **orderByDescription**  
    If true the result is ordered by Description instead of Value. Note that ordering is not always possible.  
    _Type_: boolean  
     _Optional_: True  
    _Default Value_: False  

  * **top**  
    The top clause - default is 10  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 10  

  * **skip**  
    The skip clause - default is 0  
    _Type_: int32  
     _Optional_: True  
    _Default Value_: 0  



## Business Rules

[!list limit=1000 erp.entity=Communities.NotificationSettings erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Communities.NotificationSettings erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_NotificationSettings?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_NotificationSettings?$top=10>

