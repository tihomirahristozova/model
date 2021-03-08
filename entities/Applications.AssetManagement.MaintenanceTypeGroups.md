---
uid: Applications.AssetManagement.MaintenanceTypeGroups
---
# Applications.AssetManagement.MaintenanceTypeGroups Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Represents the hierarchy of the groups of maintenance types. Entity: Eam_Maintenance_Type_Groups (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.AssetManagement.MaintenanceTypeGroups.md#code) | string | Unique code of the group. `Required` `Filter(eq;like)` `ORD` 
| [Id](Applications.AssetManagement.MaintenanceTypeGroups.md#id) | guid |  
| [Name](Applications.AssetManagement.MaintenanceTypeGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multilanguage name of the group. `Required` `Filter(eq;like)` 
| [Notes](Applications.AssetManagement.MaintenanceTypeGroups.md#notes) | string (nullable) | Notes for this MaintenanceTypeGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.AssetManagement.MaintenanceTypeGroups.md#parent) | [MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md) (nullable) | Parent group. null denotes a root group. `Filter(multi eq)` |


## Attribute Details

### Code

Unique code of the group. `Required` `Filter(eq;like)` `ORD`

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Multilanguage name of the group. `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this MaintenanceTypeGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

Parent group. null denotes a root group. `Filter(multi eq)`

_Type_: **[MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypeGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypeGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_MaintenanceTypeGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_MaintenanceTypeGroups?$top=10>

