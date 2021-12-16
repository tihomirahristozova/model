---
uid: Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes
---
# Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Defines the types of maintenances, which are allowed for assets of the different types. Entity: Eam_Managed_Asset_Type_Maintenance_Types (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{ManagedAssetType.Name:T}_  
Default Search Members:  
_ManagedAssetType.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)  
Aggregate Root:  
[Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DefaultParameterChange](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#defaultparameterchange) | int32 __nullable__ | Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means, that maintenances are not scheduled based on parameter change. 
| [DefaultScheduleDays](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#defaultscheduledays) | int32 __nullable__ | Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in days. 
| [DefaultScheduleMonths](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#defaultschedulemonths) | int32 __nullable__ | Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in months. 
| [Id](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#notes) | string (max) __nullable__ | Notes for this ManagedAssetType<br />MaintenanceType. 
| [RowVersion](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceType](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#maintenancetype) | [MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md) | The allowed maintenance type for the asset type. `Required` `Filter(multi eq)` |
| [ManagedAssetType](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#managedassettype) | [ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md) | The asset type for which the allowed maintenance type is defined. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### DefaultParameterChange

Default positive change of the tracked parameter between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means, that maintenances are not scheduled based on parameter change.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleDays

Specifies the maximum number of days between two maintenances (in addition to the number of months specified in Default Schedule Months). When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in days.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### DefaultScheduleMonths

Specifies the number of months between two maintenances. When not null, this schedule is taken with priority related to the general maintenance type schedule. null means that there is no default schedule in months.

_Type_: **int32 __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ManagedAssetTypeMaintenanceType.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceType

The allowed maintenance type for the asset type. `Required` `Filter(multi eq)`

_Type_: **[MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ManagedAssetType

The asset type for which the allowed maintenance type is defined. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetTypeMaintenanceTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetTypeMaintenanceTypes?$top=10>

