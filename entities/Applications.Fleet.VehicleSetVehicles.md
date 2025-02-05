---
uid: Applications.Fleet.VehicleSetVehicles
---
# Applications.Fleet.VehicleSetVehicles Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains lists of vehicles in the vehicle sets. Entity: Fleet_Vehicle_Set_Vehicles

## Default Visualization
Default Display Text Format:  
_{VehicleSet.Name:T}_  
Default Search Members:  
_VehicleSet.Name_  
Name Data Member:  
_VehicleSet.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Fleet.VehicleSets](Applications.Fleet.VehicleSets.md)  
Aggregate Root:  
[General.EnterpriseCompanies](General.EnterpriseCompanies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Applications.Fleet.VehicleSetVehicles.md#displaytext) | string | Uses the repository DisplayTextFormat to build the display text from the attributes and references of current object. 
| [Id](Applications.Fleet.VehicleSetVehicles.md#id) | guid |  
| [Notes](Applications.Fleet.VehicleSetVehicles.md#notes) | string (254) __nullable__ | Notes for this VehicleSetVehicle. `Filter(like)` 
| [ObjectVersion](Applications.Fleet.VehicleSetVehicles.md#objectversion) | int32 | The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking. 
| [OrdinalPos](Applications.Fleet.VehicleSetVehicles.md#ordinalpos) | int32 __nullable__ | Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. `Filter(ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleSetVehicles.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The Vehicle which is part of the vehicle set. `Required` `Filter(multi eq)` |
| [VehicleSet](Applications.Fleet.VehicleSetVehicles.md#vehicleset) | [VehicleSets](Applications.Fleet.VehicleSets.md) | The <see cref="VehicleSet"/> to which this VehicleSetVehicle belongs. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

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

### Notes

Notes for this VehicleSetVehicle. `Filter(like)`

_Type_: **string (254) __nullable__**  
_Category_: **System**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### ObjectVersion

The latest version of the extensible data object for the aggregate root for the time the object is loaded from the database. Can be used for optimistic locking.

_Type_: **int32**  
_Category_: **Extensible Data Object**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### OrdinalPos

Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. `Filter(ge;le)`

_Type_: **int32 __nullable__**  
_Category_: **System**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Vehicle

The Vehicle which is part of the vehicle set. `Required` `Filter(multi eq)`

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
_Category_: **System**  
_Supported Filters_: **Equals, EqualsIn**  

### VehicleSet

The <see cref="VehicleSet"/> to which this VehicleSetVehicle belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[VehicleSets](Applications.Fleet.VehicleSets.md)**  
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

[!list limit=1000 erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleSetVehicles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleSetVehicles?$top=10>

