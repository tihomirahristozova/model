---
uid: Applications.AssetManagement.MaintenanceTypeGroups
---
# Applications.AssetManagement.MaintenanceTypeGroups

Represents the hierarchy of the groups of maintenance types. Entity: Eam_Maintenance_Type_Groups (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.MaintenanceTypeGroups.md#Id) | guid |  
| [Code](Applications.AssetManagement.MaintenanceTypeGroups.md#Code) | string | Unique code of the group. [Required] [Filter(eq;like)] [ORD] 
| [Name](Applications.AssetManagement.MaintenanceTypeGroups.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Multilanguage name of the group. [Required] [Filter(eq;like)] 
| [Notes](Applications.AssetManagement.MaintenanceTypeGroups.md#Notes) | string (nullable) | Notes for this MaintenanceTypeGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.AssetManagement.MaintenanceTypeGroups.md#Parent) | [Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md) (nullable) | Parent group. null denotes a root group. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique code of the group. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> Multilanguage name of the group. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this MaintenanceTypeGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

> Parent group. null denotes a root group. [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypeGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypeGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.MaintenanceTypeGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_MaintenanceTypeGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_MaintenanceTypeGroups?$top=10>

