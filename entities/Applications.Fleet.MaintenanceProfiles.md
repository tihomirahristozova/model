---
uid: Applications.Fleet.MaintenanceProfiles
---
# Applications.Fleet.MaintenanceProfiles Entity

**Namespace:** [Applications.Fleet](Applications.Fleet.md)  

Profiles contain multiple maintenance plans and can be assigned directly to a vehicle. Entity: Fleet_Maintenance_Profiles

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Fleet.MaintenanceProfiles](Applications.Fleet.MaintenanceProfiles.md)  
  * [Applications.Fleet.MaintenanceProfilePlans](Applications.Fleet.MaintenanceProfilePlans.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.Fleet.MaintenanceProfiles.md#code) | string(16) | The unique code of the MaintenanceProfile. `Required` 
| [Id](Applications.Fleet.MaintenanceProfiles.md#id) | guid |  
| [IsActive](Applications.Fleet.MaintenanceProfiles.md#isactive) | boolean | True if the profile is active and can be assigned to vehicles. However, if a profile is already assigned to a vehicle, it will still work even if it is de-activated. `Required` `Default(true)` `Introduced in version 18.2` 
| [Name](Applications.Fleet.MaintenanceProfiles.md#name) | string(254) | Name of the maintenance profile (Multilanguage). `Required` 
| [Notes](Applications.Fleet.MaintenanceProfiles.md#notes) | string(2147483647) (nullable) | Notes for this MaintenanceProfile. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Plans | [MaintenanceProfilePlans](Applications.Fleet.MaintenanceProfilePlans.md) | List of `MaintenanceProfilePlan`(Applications.Fleet.MaintenanceProfilePlans.md) child objects, based on the `Applications.Fleet.MaintenanceProfilePlan.MaintenanceProfile`(Applications.Fleet.MaintenanceProfilePlans.md#maintenanceprofile) back reference 


## Attribute Details

### Code

The unique code of the MaintenanceProfile. `Required`

_Type_: **string(16)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

True if the profile is active and can be assigned to vehicles. However, if a profile is already assigned to a vehicle, it will still work even if it is de-activated. `Required` `Default(true)` `Introduced in version 18.2`

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

Name of the maintenance profile (Multilanguage). `Required`

_Type_: **string(254)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Notes

Notes for this MaintenanceProfile.

_Type_: **string(2147483647) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  



## Business Rules

[!list erp.entity=Applications.Fleet.MaintenanceProfiles erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Fleet.MaintenanceProfiles erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Fleet_MaintenanceProfiles?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Fleet_MaintenanceProfiles?$top=10>

