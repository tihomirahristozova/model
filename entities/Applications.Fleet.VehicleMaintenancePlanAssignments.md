---
uid: Applications.Fleet.VehicleMaintenancePlanAssignments
---
# Applications.Fleet.VehicleMaintenancePlanAssignments Entity

Represents assignment of a maintenance plan to a vehicle. Entity: Fleet_Vehicle_Maintenance_Plan_Assignments

Default Display Text Format:  
_{Id}_  
Default Search Member:  
_Id_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.VehicleMaintenancePlanAssignments.md#id) | guid |  
| [IsActive](Applications.Fleet.VehicleMaintenancePlanAssignments.md#isactive) | boolean | Specifies whether the plan is active. [Required] [Default(true)] 
| [LastMaintenanceMileageKm](Applications.Fleet.VehicleMaintenancePlanAssignments.md#lastmaintenancemileagekm) | int32 (nullable) | The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check. 
| [LastMaintenanceTripCount](Applications.Fleet.VehicleMaintenancePlanAssignments.md#lastmaintenancetripcount) | int32 (nullable) | The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check. 
| [Notes](Applications.Fleet.VehicleMaintenancePlanAssignments.md#notes) | string (nullable) | Notes for this VehicleMaintenance<br />PlanAssignment. 
| [StartingDate](Applications.Fleet.VehicleMaintenancePlanAssignments.md#startingdate) | date | The date on which the periodic maintenance should start. [Required] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenancePlan](Applications.Fleet.VehicleMaintenancePlanAssignments.md#maintenanceplan) | [MaintenancePlans](Applications.Fleet.MaintenancePlans.md) | The assigned periodic maintenance type. [Required] [Filter(multi eq)] |
| [Vehicle](Applications.Fleet.VehicleMaintenancePlanAssignments.md#vehicle) | [Vehicles](Applications.Fleet.Vehicles.md) | The vehicle, to which a periodic maintenance plan is assigned. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the plan is active. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### LastMaintenanceMileageKm

The mileage of the vehicle (in Kilometers), when the last maintenance of this type occurred. Should be specified for plans, which require mileage check.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### LastMaintenanceTripCount

The trip count of the vehicle, when the last maintenance of this type occurred. Should be specified for plans, which trip count check.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Notes

Notes for this VehicleMaintenancePlanAssignment.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### StartingDate

The date on which the periodic maintenance should start. [Required]

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenancePlan

The assigned periodic maintenance type. [Required] [Filter(multi eq)]

_Type_: **[MaintenancePlans](Applications.Fleet.MaintenancePlans.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Vehicle

The vehicle, to which a periodic maintenance plan is assigned. [Required] [Filter(multi eq)]

_Type_: **[Vehicles](Applications.Fleet.Vehicles.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.VehicleMaintenancePlanAssignments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_VehicleMaintenancePlanAssignments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_VehicleMaintenancePlanAssignments?$top=10>

