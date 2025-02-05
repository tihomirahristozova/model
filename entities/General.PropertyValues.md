---
uid: General.PropertyValues
---
# General.PropertyValues Entity

**Namespace:** [General](General.md)  

The actual values of the user-defined properties for each actual entity. Entity: Gen_Property_Values

## Default Visualization
Default Display Text Format:  
_{Id}: {EntityItemId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.PropertyValues](General.PropertyValues.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Description](General.PropertyValues.md#description) | [MultilanguageString (254)](../data-types.md#multilanguagestring) __nullable__ | The actual description value of the property for the specified entity (the entity with the specified Id). 
| [DisplayText](General.PropertyValues.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [EntityItemId](General.PropertyValues.md#entityitemid) | guid | The Id of the actual entity for which the value is specified. `Required` `Filter(multi eq)` 
| [Id](General.PropertyValues.md#id) | guid |  
| [ObjectVersion](General.PropertyValues.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [Picture](General.PropertyValues.md#picture) | byte[] __nullable__ | The actual picture of the property for the specified entity (the entity with the specified Id). 
| [PropertyValueField](General.PropertyValues.md#propertyvaluefield) | string (254) __nullable__ | The actual value of the property for the specified entity (the entity with the specified Id). 
| [ValueId](General.PropertyValues.md#valueid) | guid __nullable__ | The internal Id of the value of the property for the specified entity (the entity with the specified Id). For choosable properties, this contains the id of the original "allowed value" row, from which the value was derived. null for non-choosable (free-text) properties, but also for old property values (before this id was available) or other unknown values. `Filter(multi eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Property](General.PropertyValues.md#property) | [CustomProperties](General.CustomProperties.md) | The property, whose value is stored here. `Required` `Filter(multi eq)` |


## Attribute Details

### Description

The actual description value of the property for the specified entity (the entity with the specified Id).

_Type_: **[MultilanguageString (254)](../data-types.md#multilanguagestring) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### EntityItemId

The Id of the actual entity for which the value is specified. `Required` `Filter(multi eq)`

_Type_: **guid**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Picture

The actual picture of the property for the specified entity (the entity with the specified Id).

_Type_: **byte[] __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### PropertyValueField

The actual value of the property for the specified entity (the entity with the specified Id).

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ValueId

The internal Id of the value of the property for the specified entity (the entity with the specified Id). For choosable properties, this contains the id of the original "allowed value" row, from which the value was derived. null for non-choosable (free-text) properties, but also for old property values (before this id was available) or other unknown values. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  


## Reference Details

### Property

The property, whose value is stored here. `Required` `Filter(multi eq)`

_Type_: **[CustomProperties](General.CustomProperties.md)**  
_Indexed_: **True**  
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

[!list limit=1000 erp.entity=General.PropertyValues erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.PropertyValues erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_PropertyValues?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_PropertyValues?$top=10>

