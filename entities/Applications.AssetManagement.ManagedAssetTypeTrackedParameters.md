# Applications.AssetManagement.ManagedAssetTypeTrackedParameters

Defines the parameters, which are tracked for the assets of the different types. Entity: Eam_Managed_Asset_Type_Tracked_Parameters (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#Id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#Notes) | string (nullable) | Notes for this ManagedAssetTypeTrackedParameter. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ManagedAssetType](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#ManagedAssetType) | [Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md) | The asset type for which the tracked parameter is defined. [Required] [Filter(multi eq)] [Owner] |
| [TrackedParameter](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#TrackedParameter) | [Applications.AssetManagement.TrackedParameters](Applications.AssetManagement.TrackedParameters.md) | The parameter, which will be tracked for assets of the specified type. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this ManagedAssetTypeTrackedParameter.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ManagedAssetType

> The asset type for which the tracked parameter is defined. [Required] [Filter(multi eq)] [Owner]

_Type_: **[Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  

### TrackedParameter

> The parameter, which will be tracked for assets of the specified type. [Required] [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.TrackedParameters](Applications.AssetManagement.TrackedParameters.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeTrackedParameters erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeTrackedParameters erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypeTrackedParameters erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetTypeTrackedParameters?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetTypeTrackedParameters?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Eam_Managed_Asset_Type_Tracked_Parameters?$top=10>

