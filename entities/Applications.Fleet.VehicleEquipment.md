---
uid: Applications.Fleet.VehicleEquipment
---
# Applications.Fleet.VehicleEquipment

Contains the actual and history of equipment, installed on the vehicles. Entity: Fleet_Vehicle_Equipment

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.VehicleEquipment.md#Id) | guid |  
| [EndDate](Applications.Fleet.VehicleEquipment.md#EndDate) | date (nullable) | The date when the equipment was removed. null when the equipment is still installed on the vehicle. [Filter(ge;le)] 
| [Notes](Applications.Fleet.VehicleEquipment.md#Notes) | string (nullable) | Notes for the installed equipment. 
| [Quantity](Applications.Fleet.VehicleEquipment.md#Quantity) | int32 | Quantity of the equipment. [Required] [Default(1)] [Filter(ge;le)] 
| [StartDate](Applications.Fleet.VehicleEquipment.md#StartDate) | date | The installation date of the equipment. [Required] [Filter(ge;le)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EquipmentType](Applications.Fleet.VehicleEquipment.md#EquipmentType) | [Applications.Fleet.EquipmentTypes](Applications.Fleet.EquipmentTypes.md) | The type of equipment installed on the vehicle. [Required] [Filter(multi eq)] |
| [Vehicle](Applications.Fleet.VehicleEquipment.md#Vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The vehicle that is holding the equipment. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### EndDate

> The date when the equipment was removed. null when the equipment is still installed on the vehicle. [Filter(ge;le)]

_Type_: **date (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Notes

> Notes for the installed equipment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Quantity

> Quantity of the equipment. [Required] [Default(1)] [Filter(ge;le)]

_Type_: **int32**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  
_Default Value_: **1**  

### StartDate

> The installation date of the equipment. [Required] [Filter(ge;le)]

_Type_: **date**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  


## Reference Details

### EquipmentType

> The type of equipment installed on the vehicle. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.EquipmentTypes](Applications.Fleet.EquipmentTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Vehicle

> The vehicle that is holding the equipment. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleEquipment erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleEquipment erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleEquipment erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleEquipment?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleEquipment?$top=10>

