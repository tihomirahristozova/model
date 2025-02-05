---
uid: Applications.Fleet.VehicleObdTroubles
---
# Applications.Fleet.VehicleObdTroubles Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains troubles, reported by the on-board diagnostics (OBD) of the vehicle. Entity: Fleet_Vehicle_Obd_Troubles

## Default Visualization
Default Display Text Format:  
_{DiagnosticTroubleCode}_  
Default Search Members:  
_DiagnosticTroubleCode_  
Code Data Member:  
_DiagnosticTroubleCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Fleet.VehicleObdTroubles](Applications.Fleet.VehicleObdTroubles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Details](Applications.Fleet.VehicleObdTroubles.md#details) | string (max) __nullable__ | Additional text, human-readable details for the trouble, generated by the hardware agent. Contains at least some summary data in English and optionally, locale-specific data. 
| [DiagnosticTroubleCode](Applications.Fleet.VehicleObdTroubles.md#diagnostictroublecode) | string (5) | Standartized OBD-II diagnostic trouble code. `Required` 
| [DisplayText](Applications.Fleet.VehicleObdTroubles.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Applications.Fleet.VehicleObdTroubles.md#id) | guid |  
| [ManufacturerTroubleCode](Applications.Fleet.VehicleObdTroubles.md#manufacturertroublecode) | string (16) __nullable__ | Non-standard manufacturer-specific trouble code. null when it is not available. 
| [ObjectVersion](Applications.Fleet.VehicleObdTroubles.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [OccurenceDateTime](Applications.Fleet.VehicleObdTroubles.md#occurencedatetime) | datetime | Date and time (UTC) when the trouble was detected. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleObdTroubles.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, which has experienced the trouble. `Required` `Filter(multi eq)` |


## Attribute Details

### Details

Additional text, human-readable details for the trouble, generated by the hardware agent. Contains at least some summary data in English and optionally, locale-specific data.

_Type_: **string (max) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### DiagnosticTroubleCode

Standartized OBD-II diagnostic trouble code. `Required`

_Type_: **string (5)**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **5**  

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

### ManufacturerTroubleCode

Non-standard manufacturer-specific trouble code. null when it is not available.

_Type_: **string (16) __nullable__**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### OccurenceDateTime

Date and time (UTC) when the trouble was detected. `Required`

_Type_: **datetime**  
_Category_: **System**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Vehicle

The vehicle, which has experienced the trouble. `Required` `Filter(multi eq)`

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
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

[!list limit=1000 erp.entity=Applications.Fleet.VehicleObdTroubles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleObdTroubles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleObdTroubles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleObdTroubles?$top=10>

