---
uid: Applications.Fleet.MaintenanceProfilePlans
---
# Applications.Fleet.MaintenanceProfilePlans Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Contains the plans, included in the maintenance profile. Entity: Fleet_Maintenance_Profile_Plans

## Default Visualization
Default Display Text Format:  
_{MaintenanceProfile.Code}: {MaintenanceProfile.Name:T}_  
Default Search Member:  
_MaintenanceProfile.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)  
Aggregate Root:  
[Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.MaintenanceProfilePlans.md#id) | guid |  
| [IsActive](Applications.Fleet.MaintenanceProfilePlans.md#isactive) | boolean | True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. `Required` `Default(true)` `Introduced in version 18.2` 
| [Notes](Applications.Fleet.MaintenanceProfilePlans.md#notes) | string (max) __nullable__ | Notes for this MaintenanceProfilePlan. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenancePlan](Applications.Fleet.MaintenanceProfilePlans.md#maintenanceplan) | [MaintenancePlans](Applications.Fleet.MaintenancePlans.md) | The maintenance plan, which is included in the profile. `Required` `Filter(multi eq)` |
| [MaintenanceProfile](Applications.Fleet.MaintenanceProfilePlans.md#maintenanceprofile) | [MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md) | The maintenance profile, which includes the plan. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. `Required` `Default(true)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

Notes for this MaintenanceProfilePlan.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### MaintenancePlan

The maintenance plan, which is included in the profile. `Required` `Filter(multi eq)`

_Type_: **[MaintenancePlans](Applications.Fleet.MaintenancePlans.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### MaintenanceProfile

The maintenance profile, which includes the plan. `Required` `Filter(multi eq)` `Owner`

_Type_: **[MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_MaintenanceProfilePlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_MaintenanceProfilePlans?$top=10>

