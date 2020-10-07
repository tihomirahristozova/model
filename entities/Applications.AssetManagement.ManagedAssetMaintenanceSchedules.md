# Applications.AssetManagement.ManagedAssetMaintenanceSchedules

Contains the maintenance schedules for the managed assets. Entity: Eam_Managed_Asset_Maintenance_Schedules (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#Id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#Notes) | string (nullable) | Notes for this ManagedAssetMaintenanceSchedule. 
| [ParameterChangeDelta](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#ParameterChangeDelta) | int32 (nullable) | The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. null means, that the maintenances are not planned, based on parameter change. [Filter(multi eq;ge;le)] 
| [ScheduleDays](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#ScheduleDays) | int32 (nullable) | Number of days between planned maintenances. null means that the schedule is not planned based on days. 
| [ScheduleMonths](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#ScheduleMonths) | int32 (nullable) | Number of months between planned maintenances. null means that the schedule is not planned based on months. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceType](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#MaintenanceType) | [Applications.AssetManagement.MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md) | What type of maintenance is scheduled. [Required] [Filter(multi eq)] |
| [ManagedAsset](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#ManagedAsset) | [Applications.AssetManagement.ManagedAssets](Applications.AssetManagement.ManagedAssets.md) | The managed asset for which the maintenance schedule applies. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ManagedAssetMaintenanceSchedule.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParameterChangeDelta

> The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. null means, that the maintenances are not planned, based on parameter change. [Filter(multi eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### ScheduleDays

> Number of days between planned maintenances. null means that the schedule is not planned based on days.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScheduleMonths

> Number of months between planned maintenances. null means that the schedule is not planned based on months.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceType

> What type of maintenance is scheduled. [Required] [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### ManagedAsset

> The managed asset for which the maintenance schedule applies. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.AssetManagement.ManagedAssets](Applications.AssetManagement.ManagedAssets.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetMaintenanceSchedules erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetMaintenanceSchedules erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.ManagedAssetMaintenanceSchedules erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetMaintenanceSchedules?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetMaintenanceSchedules?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Eam_Managed_Asset_Maintenance_Schedules?$top=10>

