---
uid: Applications.Fleet.VehicleMaintenancePlanAssignments
---
# Applications.Fleet.VehicleMaintenancePlanAssignments Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Represents assignment of a maintenance plan to a vehicle. Entity: Fleet_Vehicle_Maintenance_Plan_Assignments

## Default Visualization
Default Display Text Format:  
_{Id}: {VehicleId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Fleet.VehicleMaintenancePlanAssignments](Applications.Fleet.VehicleMaintenancePlanAssignments.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DisplayText](Applications.Fleet.VehicleMaintenancePlanAssignments.md#displaytext) | string |  
| [Id](Applications.Fleet.VehicleMaintenancePlanAssignments.md#id) | guid |  
| [IsActive](Applications.Fleet.VehicleMaintenancePlanAssignments.md#isactive) | boolean | Specifies whether the plan is active. `Required` `Default(true)` 
| [LastMaintenanceMileageKm](Applications.Fleet.VehicleMaintenancePlanAssignments.md#lastmaintenancemileagekm) | int32 __nullable__ | The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check. 
| [LastMaintenanceTripCount](Applications.Fleet.VehicleMaintenancePlanAssignments.md#lastmaintenancetripcount) | int32 __nullable__ | The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check. 
| [Notes](Applications.Fleet.VehicleMaintenancePlanAssignments.md#notes) | string (max) __nullable__ | Notes for this VehicleMaintenance<br />PlanAssignment. 
| [ObjectVersion](Applications.Fleet.VehicleMaintenancePlanAssignments.md#objectversion) | int32 |  
| [StartingDate](Applications.Fleet.VehicleMaintenancePlanAssignments.md#startingdate) | date | The date on which the periodic maintenance should start. `Required` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenancePlan](Applications.Fleet.VehicleMaintenancePlanAssignments.md#maintenanceplan) | [MaintenancePlans](Applications.Fleet.MaintenancePlans.md) | The assigned periodic maintenance type. `Required` `Filter(multi eq)` |
| [Vehicle](Applications.Fleet.VehicleMaintenancePlanAssignments.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, to which a periodic maintenance plan is assigned. `Required` `Filter(multi eq)` |


## Attribute Details

### DisplayText

_Type_: **string**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the plan is active. `Required` `Default(true)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LastMaintenanceMileageKm

The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LastMaintenanceTripCount

The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this VehicleMaintenancePlanAssignment.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ObjectVersion

_Type_: **int32**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: ****  

### StartingDate

The date on which the periodic maintenance should start. `Required`

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenancePlan

The assigned periodic maintenance type. `Required` `Filter(multi eq)`

_Type_: **[MaintenancePlans](Applications.Fleet.MaintenancePlans.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Vehicle

The vehicle, to which a periodic maintenance plan is assigned. `Required` `Filter(multi eq)`

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
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

[!list limit=1000 erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleMaintenancePlanAssignments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleMaintenancePlanAssignments?$top=10>

