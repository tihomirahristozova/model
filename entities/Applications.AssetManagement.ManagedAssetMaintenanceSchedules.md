---
uid: Applications.AssetManagement.ManagedAssetMaintenanceSchedules
---
# Applications.AssetManagement.ManagedAssetMaintenanceSchedules Entity

Contains the maintenance schedules for the managed assets. Entity: Eam_Managed_Asset_Maintenance_Schedules (Introduced in version 19.1)

Default Display Text Format:  
_{ManagedAsset.Code}: {ManagedAsset.Name:T}_  
Default Search Member:  
_ManagedAsset.Code_  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#notes) | string (nullable) | Notes for this ManagedAssetMaintenance<br />Schedule. 
| [ParameterChangeDelta](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#parameterchangedelta) | int32 (nullable) | The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. null means, that the maintenances are not planned, based on parameter change. [Filter(multi eq;ge;le)] 
| [ScheduleDays](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#scheduledays) | int32 (nullable) | Number of days between planned maintenances. null means that the schedule is not planned based on days. 
| [ScheduleMonths](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#schedulemonths) | int32 (nullable) | Number of months between planned maintenances. null means that the schedule is not planned based on months. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceType](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#maintenancetype) | [MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md) | What type of maintenance is scheduled. [Required] [Filter(multi eq)] |
| [ManagedAsset](Applications.AssetManagement.ManagedAssetMaintenanceSchedules.md#managedasset) | [ManagedAssets](Applications.AssetManagement.ManagedAssets.md) | The managed asset for which the maintenance schedule applies. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ManagedAssetMaintenanceSchedule.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParameterChangeDelta

The value of the tracked parameter change between planned maintenances. The tracked parameter is determined based on the Maintenance Type. null means, that the maintenances are not planned, based on parameter change. [Filter(multi eq;ge;le)]

_Type_: **int32 (nullable)**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### ScheduleDays

Number of days between planned maintenances. null means that the schedule is not planned based on days.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ScheduleMonths

Number of months between planned maintenances. null means that the schedule is not planned based on months.

_Type_: **int32 (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceType

What type of maintenance is scheduled. [Required] [Filter(multi eq)]

_Type_: **[MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ManagedAsset

The managed asset for which the maintenance schedule applies. [Required] [Filter(multi eq)] [Owner]

_Type_: **[ManagedAssets](Applications.AssetManagement.ManagedAssets.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetMaintenanceSchedules erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetMaintenanceSchedules erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetMaintenanceSchedules?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetMaintenanceSchedules?$top=10>

