---
uid: General.Contacts.PartyRelationships
---
# General.Contacts.PartyRelationships Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Defines the relationships between the parties. The data is preserved over time. Entity: Cm_Party_Relationships

## Default Visualization
Default Display Text Format:  
_{Id}: {FromPartyId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [General.Contacts.PartyRelationships](General.Contacts.PartyRelationships.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](General.Contacts.PartyRelationships.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [FromDate](General.Contacts.PartyRelationships.md#fromdate) | datetime __nullable__ | The starting date of the relationship. null means the date is the begining of the time. `Filter(ge;le)` 
| [Id](General.Contacts.PartyRelationships.md#id) | guid |  
| [Notes](General.Contacts.PartyRelationships.md#notes) | string (254) __nullable__ | Notes for this PartyRelationship. 
| [ObjectVersion](General.Contacts.PartyRelationships.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [ToDate](General.Contacts.PartyRelationships.md#todate) | datetime __nullable__ | The ending date of the relationship. null means the relationship is still active. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [FromParty](General.Contacts.PartyRelationships.md#fromparty) | [Parties](General.Contacts.Parties.md) | The first party in the relationship. `Required` `Filter(multi eq)` |
| [RelationshipType](General.Contacts.PartyRelationships.md#relationshiptype) | [PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md) | The type of the relationship. `Required` `Filter(multi eq)` |
| [ToParty](General.Contacts.PartyRelationships.md#toparty) | [Parties](General.Contacts.Parties.md) | The second party in the relationship. `Required` `Filter(multi eq)` |


## Attribute Details

### DisplayText

Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object.

_Type_: **string**  
_Category_: **Calculated Attributes**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### FromDate

The starting date of the relationship. null means the date is the begining of the time. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this PartyRelationship.

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### ToDate

The ending date of the relationship. null means the relationship is still active. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### FromParty

The first party in the relationship. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### RelationshipType

The type of the relationship. `Required` `Filter(multi eq)`

_Type_: **[PartyRelationshipTypes](General.Contacts.PartyRelationshipTypes.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### ToParty

The second party in the relationship. `Required` `Filter(multi eq)`

_Type_: **[Parties](General.Contacts.Parties.md)**  
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

[!list limit=1000 erp.entity=General.Contacts.PartyRelationships erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Contacts.PartyRelationships erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_PartyRelationships?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_PartyRelationships?$top=10>

