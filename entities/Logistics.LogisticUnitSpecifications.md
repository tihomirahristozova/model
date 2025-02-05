---
uid: Logistics.LogisticUnitSpecifications
---
# Logistics.LogisticUnitSpecifications Entity

**Namespace:** [Logistics](Logistics.md)  

Specification of a logistic unit. The database can contain any kind of specification, but most client applications and integrated methods process GS1 specifications (application codes). Entity: Log_Logistic_Unit_Specifications (Introduced in version 21.1.0.77)

## Default Visualization
Default Display Text Format:  
_{Name:T}_  
Default Search Members:  
_Code; Name_  
Code Data Member:  
_Code_  
Name Data Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Logistics.LogisticUnits](Logistics.LogisticUnits.md)  
Aggregate Root:  
[Logistics.LogisticUnits](Logistics.LogisticUnits.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Logistics.LogisticUnitSpecifications.md#code) | string (32) | The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces. `Required` `Filter(multi eq;like)` 
| [DisplayText](Logistics.LogisticUnitSpecifications.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Logistics.LogisticUnitSpecifications.md#id) | guid |  
| [Name](Logistics.LogisticUnitSpecifications.md#name) | [MultilanguageString (254)](../data-types.md#multilanguagestring) __nullable__ | Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (null). `Filter(eq;like)` 
| [Notes](Logistics.LogisticUnitSpecifications.md#notes) | string (max) __nullable__ | Notes for this LogisticUnitSpecification. 
| [ObjectVersion](Logistics.LogisticUnitSpecifications.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [Value](Logistics.LogisticUnitSpecifications.md#value) | string (254) __nullable__ | Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces. `Filter(eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [LogisticUnit](Logistics.LogisticUnitSpecifications.md#logisticunit) | [LogisticUnits](Logistics.LogisticUnits.md) | The logistic unit, which is detailed by this specification. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Code

The code of the specification, unique within the logistic unit. It can contain only alphanumeric characters and cannot contain spaces. `Required` `Filter(multi eq;like)`

_Type_: **string (32)**  
_Category_: **System**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **32**  

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

### Name

Multi-language name of the specification. For some processing purposes, the name might be contained within the client implementation and not saved to the database (null). `Filter(eq;like)`

_Type_: **[MultilanguageString (254)](../data-types.md#multilanguagestring) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this LogisticUnitSpecification.

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Value

Text value of the specification. If this is GS1 specification, it can contain only numbers and letters and cannot contain spaces. `Filter(eq;like)`

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### LogisticUnit

The logistic unit, which is detailed by this specification. `Required` `Filter(multi eq)` `Owner`

_Type_: **[LogisticUnits](Logistics.LogisticUnits.md)**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  


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

[!list limit=1000 erp.entity=Logistics.LogisticUnitSpecifications erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Logistics.LogisticUnitSpecifications erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Logistics_LogisticUnitSpecifications?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Logistics_LogisticUnitSpecifications?$top=10>

