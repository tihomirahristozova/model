---
uid: Applications.AssetManagement.ManagedAssetTypes
---
# Applications.AssetManagement.ManagedAssetTypes Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Types of managed assets. Used to categorize the assets and the tracked parameters for each type. Entity: Eam_Managed_Asset_Types (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{Code}: {Name:T}_  
Default Search Member:  
_Code_  

## Aggregate
  @aggregates  
Aggregate Tree  
* [Applications.AssetManagement.ManagedAssetTypes](Applications.AssetManagement.ManagedAssetTypes.md)  
  * [Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md)  
  * [Applications.AssetManagement.ManagedAssetTypeTrackedParameters](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.AssetManagement.ManagedAssetTypes.md#code) | string | Unique code of the asset type. [Required] [Filter(multi eq;like)] [ORD] 
| [Id](Applications.AssetManagement.ManagedAssetTypes.md#id) | guid |  
| [IsActive](Applications.AssetManagement.ManagedAssetTypes.md#isactive) | boolean | Specifies whether the asset type is active for choosing in drop-down choices. [Required] [Default(true)] 
| [Name](Applications.AssetManagement.ManagedAssetTypes.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Multilanguage name of the asset type. [Required] [Filter(multi eq;like)] 
| [Notes](Applications.AssetManagement.ManagedAssetTypes.md#notes) | string (nullable) | Notes for this ManagedAssetType. 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| MaintenanceTypes | [ManagedAssetTypeMaintenanceTypes](Applications.AssetManagement.ManagedAssetTypeMaintenanceTypes.md) | List of [ManagedAssetType<br />MaintenanceType](Applications.AssetManagement.ManagedAssetType<br />MaintenanceTypes.md) child objects, based on the [Applications.AssetManagement.ManagedAssetType<br />MaintenanceType.ManagedAssetType](Applications.AssetManagement.ManagedAssetType<br />MaintenanceTypes.md#managedassettype) back reference 
| TrackedParameters | [ManagedAssetTypeTrackedParameters](Applications.AssetManagement.ManagedAssetTypeTrackedParameters.md) | List of [ManagedAssetType<br />TrackedParameter](Applications.AssetManagement.ManagedAssetType<br />TrackedParameters.md) child objects, based on the [Applications.AssetManagement.ManagedAssetType<br />TrackedParameter.ManagedAssetType](Applications.AssetManagement.ManagedAssetType<br />TrackedParameters.md#managedassettype) back reference 


## Attribute Details

### Code

Unique code of the asset type. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the asset type is active for choosing in drop-down choices. [Required] [Default(true)]

_Type_: **boolean**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### Name

Multilanguage name of the asset type. [Required] [Filter(multi eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  

### Notes

Notes for this ManagedAssetType.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetTypes?$top=10>

