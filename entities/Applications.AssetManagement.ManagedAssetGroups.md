---
uid: Applications.AssetManagement.ManagedAssetGroups
---
# Applications.AssetManagement.ManagedAssetGroups Entity

Organizational hierarchy of asset groups. Entity: Eam_Managed_Asset_Groups (Introduced in version 19.1)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.AssetManagement.ManagedAssetGroups.md#code) | string | Unique (within all groups) code of the asset group. [Required] [Filter(multi eq;like)] [ORD] 
| [Id](Applications.AssetManagement.ManagedAssetGroups.md#id) | guid |  
| [Name](Applications.AssetManagement.ManagedAssetGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the asset group (multi-language). [Required] [Filter(eq;like)] 
| [Notes](Applications.AssetManagement.ManagedAssetGroups.md#notes) | string (nullable) | Notes for this ManagedAssetGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.AssetManagement.ManagedAssetGroups.md#parent) | [ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md) (nullable) | The parent asset group in the hierarchy. null means this is a root group. [Filter(multi eq)] |


## Attribute Details

### Code

Unique (within all groups) code of the asset group. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the asset group (multi-language). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this ManagedAssetGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

The parent asset group in the hierarchy. null means this is a root group. [Filter(multi eq)]

_Type_: **[ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.AssetManagement.ManagedAssetGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.AssetManagement.ManagedAssetGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetGroups?$top=10>

