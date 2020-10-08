---
uid: Applications.AssetManagement.ManagedAssetTypes
---
# Applications.AssetManagement.ManagedAssetTypes

Types of managed assets. Used to categorize the assets and the tracked parameters for each type. Entity: Eam_Managed_Asset_Types (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ManagedAssetTypes.md#Id) | guid |  
| [IsActive](Applications.AssetManagement.ManagedAssetTypes.md#IsActive) | boolean | Specifies whether the asset type is active for choosing in drop-down choices. [Required] [Default(true)] 
| [Code](Applications.AssetManagement.ManagedAssetTypes.md#Code) | string | Unique code of the asset type. [Required] [Filter(multi eq;like)] [ORD] 
| [Name](Applications.AssetManagement.ManagedAssetTypes.md#Name) | [MultilanguageString](../data-types.md#MultilanguageString) | Multilanguage name of the asset type. [Required] [Filter(multi eq;like)] 
| [Notes](Applications.AssetManagement.ManagedAssetTypes.md#Notes) | string (nullable) | Notes for this ManagedAssetType. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| MaintenanceTypes | [Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md) | List of [ManagedAssetTypeMaintenanceType](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md) child objects, based on the [Applications.AssetManagement.ManagedAssetTypeMaintenanceType.ManagedAssetType](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md#ManagedAssetType) back reference 
| TrackedParameters | [Applications.AssetManagement.ManagedAssetTypeTrackedParameters](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md) | List of [ManagedAssetTypeTrackedParameter](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md) child objects, based on the [Applications.AssetManagement.ManagedAssetTypeTrackedParameter.ManagedAssetType](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md#ManagedAssetType) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### IsActive

> Specifies whether the asset type is active for choosing in drop-down choices. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Code

> Unique code of the asset type. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Name

> Multilanguage name of the asset type. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#MultilanguageString)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

> Notes for this ManagedAssetType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetTypes?$top=10>

