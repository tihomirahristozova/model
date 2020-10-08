---
uid: Applications.AssetManagement.MaintenanceTypes
---
# Applications.AssetManagement.MaintenanceTypes

Types of maintenances which can be scheduled and performed on the managed assets. Maintenances can be scheduled based on date and tracked parameter change. Entity: Eam_Maintenance_Types (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.MaintenanceTypes.md#Id) | guid |  
| [DefaultParameterChange](Applications.AssetManagement.MaintenanceTypes.md#DefaultParameterChange) | int32 (nullable) | Default positive change of the tracked parameter between two maintenances. null means, that maintenances are not scheduled based on parameter change. 
| [DefaultScheduleDays](Applications.AssetManagement.MaintenanceTypes.md#DefaultScheduleDays) | int32 (nullable) | Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). null means that there is no default schedule in days. 
| [DefaultScheduleMonths](Applications.AssetManagement.MaintenanceTypes.md#DefaultScheduleMonths) | int32 (nullable) | Specifies the maximum number of months between two maintenances. null means that there is no default schedule in months. 
| [Description](Applications.AssetManagement.MaintenanceTypes.md#Description) | [MultilanguageString](../data-types.md#MultilanguageString) (nullable) | Detailed description of the maintenance (multilanguage). 
| [Code](Applications.AssetManagement.MaintenanceTypes.md#Code) | string | Unique code of the maintenance type. [Required] [Filter(eq;like)] [ORD] 
| [Name](Applications.AssetManagement.MaintenanceTypes.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Multilanguage name of the maintenance type. [Required] [Filter(eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceTypeGroup](Applications.AssetManagement.MaintenanceTypes.md#MaintenanceTypeGroup) | [Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md) | The group, to which this maintenance type belongs. [Required] [Filter(multi eq)] |
| [TrackedParameter](Applications.AssetManagement.MaintenanceTypes.md#TrackedParameter) | [Applications.AssetManagement.TrackedParameters](Applications.AssetManagement.TrackedParameters.md) (nullable) | Specifies the parameter, on which the next scheduled maintenance will be based. null means that there is no default schedule, based on parameter. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### DefaultParameterChange

> Default positive change of the tracked parameter between two maintenances. null means, that maintenances are not scheduled based on parameter change.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleDays

> Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). null means that there is no default schedule in days.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleMonths

> Specifies the maximum number of months between two maintenances. null means that there is no default schedule in months.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Description

> Detailed description of the maintenance (multilanguage).

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString) (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Code

> Unique code of the maintenance type. [Required] [Filter(eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **True**  

### Name

> Multilanguage name of the maintenance type. [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceTypeGroup

> The group, to which this maintenance type belongs. [Required] [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.MaintenanceTypeGroups](Applications.AssetManagement.MaintenanceTypeGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TrackedParameter

> Specifies the parameter, on which the next scheduled maintenance will be based. null means that there is no default schedule, based on parameter. [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.TrackedParameters](Applications.AssetManagement.TrackedParameters.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.MaintenanceTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.MaintenanceTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_MaintenanceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_MaintenanceTypes?$top=10>

