---
uid: Communities.Social.Posts
---
# Communities.Social.Posts Entity

**Namespace:** [Communities.Social](Communities.Social.md)  

User post in a social group. Entity: Cmm_Social_Posts (Introduced in version 20.1)

## Default Visualization
Default Display Text Format:  
_{Id}: {SocialGroupId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Communities.Social.Posts](Communities.Social.Posts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CreationTimeUtc](Communities.Social.Posts.md#creationtimeutc) | datetime | The exact server time (in UTC), when the post was created. `Required` 
| [DisplayText](Communities.Social.Posts.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Communities.Social.Posts.md#id) | guid |  
| [LastInteractionTimeUtc](Communities.Social.Posts.md#lastinteractiontimeutc) | datetime | The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. `Required` 
| [ObjectVersion](Communities.Social.Posts.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [PostText](Communities.Social.Posts.md#posttext) | string (max) | The post contents in clear text. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [SocialGroup](Communities.Social.Posts.md#socialgroup) | [Groups](Communities.Social.Groups.md) | The group in which the post is made. `Required` `Filter(multi eq)` |
| [User](Communities.Social.Posts.md#user) | [Users](Systems.Security.Users.md) | The user, who made the post. `Required` `Filter(multi eq)` |


## Attribute Details

### CreationTimeUtc

The exact server time (in UTC), when the post was created. `Required`

_Type_: **datetime**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### LastInteractionTimeUtc

The server time (in UTC) of the last interaction with the post, including comments, replies, likes, etc. `Required`

_Type_: **datetime**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### PostText

The post contents in clear text. `Required`

_Type_: **string (max)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### SocialGroup

The group in which the post is made. `Required` `Filter(multi eq)`

_Type_: **[Groups](Communities.Social.Groups.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### User

The user, who made the post. `Required` `Filter(multi eq)`

_Type_: **[Users](Systems.Security.Users.md)**  
_Category_: **System**  
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


### CreateNotification

Creates a notification a sends a real time event to the user.  
_Return Type_: **void**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  

**Parameters**  
  * **user**  
    The user.  
    _Type_: [Users](Systems.Security.Users.md)  

  * **notificationClass**  
    The notification class.  
    _Type_: string  

  * **subject**  
    The subject.  
    _Type_: string  


### CreateCopy

Duplicates the object and its child objects belonging to the same aggregate.              The duplicated objects are not saved to the data source but remain in the same transaction as the original object.  
_Return Type_: **EntityObject**  
_Declaring Type_: **EntityObject**  
_Domain API Request_: **POST**  


## Business Rules

[!list limit=1000 erp.entity=Communities.Social.Posts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Communities.Social.Posts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Communities_Social_Posts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Communities_Social_Posts?$top=10>

