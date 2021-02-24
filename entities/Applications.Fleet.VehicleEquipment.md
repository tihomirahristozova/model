---
uid: Applications.Fleet.VehicleEquipment
---
# Applications.Fleet.VehicleEquipment Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains the actual and history of equipment, installed on the vehicles. Entity: Fleet_Vehicle_Equipment

## Default Visualization
Default Display Text Format:  
_{Vehicle.EngineIdentificationNumber}_  
Default Search Member:  
_Vehicle.EngineIdentificationNumber_  

## Aggregate
  @aggregates  
Aggregate Parent:  
[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)  
Aggregate Root:  
[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [EndDate](Applications.Fleet.VehicleEquipment.md#enddate) | date (nullable) | The date when the equipment was removed. null when the equipment is still installed on the vehicle. [Filter(ge;le)] 
| [Id](Applications.Fleet.VehicleEquipment.md#id) | guid |  
| [Notes](Applications.Fleet.VehicleEquipment.md#notes) | string (nullable) | Notes for the installed equipment. 
| [Quantity](Applications.Fleet.VehicleEquipment.md#quantity) | int32 | Quantity of the equipment. [Required] [Default(1)] [Filter(ge;le)] 
| [StartDate](Applications.Fleet.VehicleEquipment.md#startdate) | date | The installation date of the equipment. [Required] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EquipmentType](Applications.Fleet.VehicleEquipment.md#equipmenttype) | [EquipmentTypes](Applications.Fleet.EquipmentTypes.md) | The type of equipment installed on the vehicle. [Required] [Filter(multi eq)] |
| [Vehicle](Applications.Fleet.VehicleEquipment.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The vehicle that is holding the equipment. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### EndDate

The date when the equipment was removed. null when the equipment is still installed on the vehicle. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for the installed equipment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

Quantity of the equipment. [Required] [Default(1)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### StartDate

The installation date of the equipment. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EquipmentType

The type of equipment installed on the vehicle. [Required] [Filter(multi eq)]

_Type_: **[EquipmentTypes](Applications.Fleet.EquipmentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Vehicle

The vehicle that is holding the equipment. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleEquipment erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleEquipment erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleEquipment?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleEquipment?$top=10>

