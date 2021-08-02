---
uid: Applications.AssetManagement.ManagedAssetScheduledMaintenances
---
# Applications.AssetManagement.ManagedAssetScheduledMaintenances Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Contains the scheduled maintenances for the managed assets. Each maintenance can be planned based on date, parameter value or both. Past maintenance plans are kept only for reference and can be deleted at any time. Entity: Eam_Managed_Asset_Scheduled_Maintenances (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{ManagedAsset.Code}: {ManagedAsset.Name:T}_  
Default Search Member:  
_ManagedAsset.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.AssetManagement.ManagedAssets](Applications.AssetManagement.ManagedAssets.md)  
Aggregate Root:  
[Applications.AssetManagement.ManagedAssets](Applications.AssetManagement.ManagedAssets.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Date](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#date) | date __nullable__ | The date, when the maintenance is planned. null means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met. `Filter(multi eq;ge;le)` 
| [Id](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#id) | guid |  
| [IsDismissed](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#isdismissed) | boolean | Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action. `Required` `Default(false)` `Filter(multi eq)` 
| [Notes](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#notes) | string (max) __nullable__ | Notes for this ManagedAssetScheduled<br />Maintenance. 
| [TrackedParameterValue](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#trackedparametervalue) | int32 __nullable__ | The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. null means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met. `Filter(multi eq;ge;le)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [MaintenanceType](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#maintenancetype) | [MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md) | The type of maintenance, which will be performed. `Required` `Filter(multi eq)` |
| [ManagedAsset](Applications.AssetManagement.ManagedAssetScheduledMaintenances.md#managedasset) | [ManagedAssets](Applications.AssetManagement.ManagedAssets.md) | The asset, which will be maintained. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### Date

The date, when the maintenance is planned. null means, that the plan is not related to date, but to tracked parameter value. If both date and parameter are specified, the maintenance is performed when any of the conditions is met. `Filter(multi eq;ge;le)`

_Type_: **date __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsDismissed

Specifies whether the notification for the maintenance is dismissed and the planner has decided the course of action. `Required` `Default(false)` `Filter(multi eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **False**  

### Notes

Notes for this ManagedAssetScheduledMaintenance.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### TrackedParameterValue

The value of the tracked parameter (as specified in the maintenance type) at which the maintenance will be performed. For example, for a car, we can schedule maintenance at 20,000 km mileage. null means, that the maintenance is not planned based on parameter, but rather only for date. If both date and parameter are specified, the maintenance is performed when any of the conditions is met. `Filter(multi eq;ge;le)`

_Type_: **int32 __nullable__**  
_Supported Filters_: **Equals, GreaterThanOrLessThan, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### MaintenanceType

The type of maintenance, which will be performed. `Required` `Filter(multi eq)`

_Type_: **[MaintenanceTypes](Applications.AssetManagement.MaintenanceTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### ManagedAsset

The asset, which will be maintained. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ManagedAssets](Applications.AssetManagement.ManagedAssets.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetScheduledMaintenances erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetScheduledMaintenances erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetScheduledMaintenances?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetScheduledMaintenances?$top=10>

