---
uid: Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes
---
# Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes

Defines the types of maintenances, which are allowed for assets of the different types. Entity: Eam_Managed_Asset_Type_Maintenance_Types (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultParameterChange](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#defaultparameterchange) | int32 (nullable) | Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means, that maintenances are not scheduled based on parameter change. 
| [DefaultScheduleDays](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#defaultscheduledays) | int32 (nullable) | Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in days. 
| [DefaultScheduleMonths](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#defaultschedulemonths) | int32 (nullable) | Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in months. 
| [Id](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#notes) | string (nullable) | Notes for this ManagedAssetTypeMaintenanceType. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceType](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#maintenancetype) | [Applications.AssetManagement.MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md) | The allowed maintenance type for the asset type. [Required] [Filter(multi eq)] |
| [ManagedAssetType](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#managedassettype) | [Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md) | The asset type for which the allowed maintenance type is defined. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### DefaultParameterChange

> Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means, that maintenances are not scheduled based on parameter change.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleDays

> Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in days.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleMonths

> Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in months.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ManagedAssetTypeMaintenanceType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceType

> The allowed maintenance type for the asset type. [Required] [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ManagedAssetType

> The asset type for which the allowed maintenance type is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetTypeMaintenanceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetTypeMaintenanceTypes?$top=10>

