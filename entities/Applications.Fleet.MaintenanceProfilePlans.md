# Applications.Fleet.MaintenanceProfilePlans

Contains the plans, included in the maintenance profile. Entity: Fleet_Maintenance_Profile_Plans

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Fleet.MaintenanceProfilePlans.md#Id) | guid |  
| [IsActive](Applications.Fleet.MaintenanceProfilePlans.md#IsActive) | boolean | True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. [Required] [Default(true)] (Introduced in version 18.2.100.0) 
| [Notes](Applications.Fleet.MaintenanceProfilePlans.md#Notes) | string (nullable) | Notes for this MaintenanceProfilePlan. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenancePlan](Applications.Fleet.MaintenanceProfilePlans.md#MaintenancePlan) | [Applications.Fleet.MaintenancePlans](Applications.Fleet.MaintenancePlans.md) | The maintenance plan, which is included in the profile. [Required] [Filter(multi eq)] |
| [MaintenanceProfile](Applications.Fleet.MaintenanceProfilePlans.md#MaintenanceProfile) | [Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md) | The maintenance profile, which includes the plan. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> True if the maintenance plan is active for this profile. When a plan is not active, maintenance for it will not occur for the current profile. [Required] [Default(true)] (Introduced in version 18.2.100.0)

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Notes

> Notes for this MaintenanceProfilePlan.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenancePlan

> The maintenance plan, which is included in the profile. [Required] [Filter(multi eq)]

_Type_: **[Applications.Fleet.MaintenancePlans](Applications.Fleet.MaintenancePlans.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### MaintenanceProfile

> The maintenance profile, which includes the plan. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Fleet.MaintenanceProfilePlans erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_MaintenanceProfilePlans?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_MaintenanceProfilePlans?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Fleet_Maintenance_Profile_Plans?$top=10>

