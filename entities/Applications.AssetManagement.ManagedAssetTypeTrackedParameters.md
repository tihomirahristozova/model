---
uid: Applications.AssetManagement.ManagedAssetTypeTrackedParameters
---
# Applications.AssetManagement.ManagedAssetTypeTrackedParameters Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Defines the parameters, which are tracked for the assets of the different types. Entity: Eam_Managed_Asset_Type_Tracked_Parameters (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{ManagedAssetType.Code}: {ManagedAssetType.Name:T}_  
Default Search Member:  
_ManagedAssetType.Code_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)  
Aggregate Root:  
[Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#notes) | string (nullable) | Notes for this ManagedAssetType<br />TrackedParameter. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ManagedAssetType](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#managedassettype) | [ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md) | The asset type for which the tracked parameter is defined. `Required` `Filter(multi eq)` `Owner` |
| [TrackedParameter](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#trackedparameter) | [TrackedParameters](Applications.AssetManagement.TrackedParameters.md) | The parameter, which will be tracked for assets of the specified type. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this ManagedAssetTypeTrackedParameter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ManagedAssetType

The asset type for which the tracked parameter is defined. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### TrackedParameter

The parameter, which will be tracked for assets of the specified type. `Required` `Filter(multi eq)`

_Type_: **[TrackedParameters](Applications.AssetManagement.TrackedParameters.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeTrackedParameters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeTrackedParameters erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetTypeTrackedParameters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetTypeTrackedParameters?$top=10>

