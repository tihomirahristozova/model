---
uid: Applications.Fleet.VehicleMaintenancePlanAssignments
---
# Applications.Fleet.VehicleMaintenancePlanAssignments

Represents assignment of a maintenance plan to a vehicle. Entity: Fleet_Vehicle_Maintenance_Plan_Assignments

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.VehicleMaintenancePlanAssignments.md#Id) | guid |  
| [IsActive](Applications.Fleet.VehicleMaintenancePlanAssignments.md#IsActive) | boolean | Specifies whether the plan is active. [Required] [Default(true)] 
| [LastMaintenanceMileageKm](Applications.Fleet.VehicleMaintenancePlanAssignments.md#LastMaintenanceMileageKm) | int32 (nullable) | The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check. 
| [LastMaintenanceTripCount](Applications.Fleet.VehicleMaintenancePlanAssignments.md#LastMaintenanceTripCount) | int32 (nullable) | The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check. 
| [Notes](Applications.Fleet.VehicleMaintenancePlanAssignments.md#Notes) | string (nullable) | Notes for this VehicleMaintenancePlanAssignment. 
| [StartingDate](Applications.Fleet.VehicleMaintenancePlanAssignments.md#StartingDate) | date | The date on which the periodic maintenance should start. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenancePlan](Applications.Fleet.VehicleMaintenancePlanAssignments.md#MaintenancePlan) | [Applications.Fleet.MaintenancePlans](Applications.Fleet.MaintenancePlans.md) | The assigned periodic maintenance type. [Required] [Filter(multi eq)] |
| [Vehicle](Applications.Fleet.VehicleMaintenancePlanAssignments.md#Vehicle) | [Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, to which a periodic maintenance plan is assigned. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Specifies whether the plan is active. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LastMaintenanceMileageKm

> The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LastMaintenanceTripCount

> The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

> Notes for this VehicleMaintenancePlanAssignment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartingDate

> The date on which the periodic maintenance should start. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenancePlan

> The assigned periodic maintenance type. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.MaintenancePlans](Applications.Fleet.MaintenancePlans.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### Vehicle

> The vehicle, to which a periodic maintenance plan is assigned. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleMaintenancePlanAssignments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleMaintenancePlanAssignments?$top=10>

