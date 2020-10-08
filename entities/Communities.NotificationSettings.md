---
uid: Communities.NotificationSettings
---
# Communities.NotificationSettings

User notification settings for the different notification classes. Entity: Cmm_Notification_Settings (Introduced in version 20.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Communities.NotificationSettings.md#id) | guid |  
| [NotificationClass](Communities.NotificationSettings.md#notificationclass) | string (nullable) | The class of the notification, for which the user is specifying settings. When null, the setting is applied to all notification classes. [Filter(multi eq)] 
| [ReceiveMail](Communities.NotificationSettings.md#receivemail) | boolean | True if the user should receive mail. [Required] [Default(false)] [Filter(eq)] 
| [ReceiveNotification](Communities.NotificationSettings.md#receivenotification) | boolean | True if the user should receive internal notification. [Required] [Default(true)] [Filter(eq)] 
| [ReceiveSms](Communities.NotificationSettings.md#receivesms) | boolean | True if the user should receive SMS. [Required] [Default(false)] [Filter(eq)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [User](Communities.NotificationSettings.md#user) | [Systems.Security.Users](Systems.Security.Users.md) | The user for whom the notification setting is about. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### NotificationClass

> The class of the notification, for which the user is specifying settings. When null, the setting is applied to all notification classes. [Filter(multi eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ReceiveMail

> True if the user should receive mail. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### ReceiveNotification

> True if the user should receive internal notification. [Required] [Default(true)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### ReceiveSms

> True if the user should receive SMS. [Required] [Default(false)] [Filter(eq)]

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **False**  


## Reference Details

### User

> The user for whom the notification setting is about. [Required] [Filter(multi eq)]

_Type_: **[Systems.Security.Users](Systems.Security.Users.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Communities.NotificationSettings erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Communities.NotificationSettings erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Communities.NotificationSettings erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_NotificationSettings?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_NotificationSettings?$top=10>

