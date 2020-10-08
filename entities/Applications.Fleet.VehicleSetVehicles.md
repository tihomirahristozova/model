---
uid: Applications.Fleet.VehicleSetVehicles
---
# Applications.Fleet.VehicleSetVehicles

Contains lists of vehicles in the vehicle sets. Entity: Fleet_Vehicle_Set_Vehicles

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.VehicleSetVehicles.md#Id) | guid |  
| [Notes](Applications.Fleet.VehicleSetVehicles.md#Notes) | string (nullable) | Notes for this VehicleSetVehicle. [Filter(like)] 
| [OrdinalPos](Applications.Fleet.VehicleSetVehicles.md#OrdinalPos) | int32 (nullable) | Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Vehicle](Applications.Fleet.VehicleSetVehicles.md#Vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The Vehicle which is part of the vehicle set. [Required] [Filter(multi eq)] |
| [VehicleSet](Applications.Fleet.VehicleSetVehicles.md#VehicleSet) | [Applications.Fleet.VehicleSets](Applications.Fleet.VehicleSets.md) | The [VehicleSet](Applications.Fleet.VehicleSetVehicles.md#VehicleSet) to which this VehicleSetVehicle belongs. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this VehicleSetVehicle. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### OrdinalPos

> Ordinal position of the vehicle within the vehicle set. Position 0 has special meaning - this is the leading vehicle. [Filter(ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### Vehicle

> The Vehicle which is part of the vehicle set. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### VehicleSet

> The [VehicleSet](Applications.Fleet.VehicleSetVehicles.md#VehicleSet) to which this VehicleSetVehicle belongs. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Fleet.VehicleSets](Applications.Fleet.VehicleSets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleSetVehicles erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleSetVehicles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleSetVehicles?$top=10>

