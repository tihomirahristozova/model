---
uid: Applications.Fleet.VehicleAlerts
---
# Applications.Fleet.VehicleAlerts Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains alerts, specific to one vehicle. Alerts are created based on many sources and stay active, until excplicitly hidden. Entity: Fleet_Vehicle_Alerts

## Default Visualization
Default Display Text Format:  
_{Id}: {VehicleId}_  
Default Search Members:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Fleet.VehicleAlerts](Applications.Fleet.VehicleAlerts.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [AlertType](Applications.Fleet.VehicleAlerts.md#alerttype) | string (3) | The type of the alert. The type is specfic to the Source. `Required` 
| [Description](Applications.Fleet.VehicleAlerts.md#description) | string (254) | Description of the alert (Multilanguage). `Required` 
| [Id](Applications.Fleet.VehicleAlerts.md#id) | guid |  
| [IsHidden](Applications.Fleet.VehicleAlerts.md#ishidden) | boolean | Specifies, whether the alert is hidden (e.g. managed by the responsible person). `Required` `Default(false)` 
| [Source](Applications.Fleet.VehicleAlerts.md#source) | string (1) | The source of the alert. G=GPS, O=OBD, M=Maintenance. `Required` 
| [Time](Applications.Fleet.VehicleAlerts.md#time) | datetime | The time of the alert. `Required` `ORD` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleAlerts.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, for which is the alert. `Required` `Filter(multi eq)` |


## Attribute Details

### AlertType

The type of the alert. The type is specfic to the Source. `Required`

_Type_: **string (3)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **3**  

### Description

Description of the alert (Multilanguage). `Required`

_Type_: **string (254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsHidden

Specifies, whether the alert is hidden (e.g. managed by the responsible person). `Required` `Default(false)`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Source

The source of the alert. G=GPS, O=OBD, M=Maintenance. `Required`

_Type_: **string (1)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **1**  

### Time

The time of the alert. `Required` `ORD`

_Type_: **datetime**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  


## Reference Details

### Vehicle

The vehicle, for which is the alert. `Required` `Filter(multi eq)`

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleAlerts erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Fleet.VehicleAlerts erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleAlerts?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleAlerts?$top=10>

