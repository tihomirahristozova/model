---
uid: Applications.AssetManagement.ManagedAssetGroups
---
# Applications.AssetManagement.ManagedAssetGroups Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Organizational hierarchy of asset groups. Entity: Eam_Managed_Asset_Groups (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{Name:T} : {Code}_  
Default Search Member:  
_Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.AssetManagement.ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Code](Applications.AssetManagement.ManagedAssetGroups.md#code) | string (16) | Unique (within all groups) code of the asset group. `Required` `Filter(multi eq;like)` `ORD` 
| [Id](Applications.AssetManagement.ManagedAssetGroups.md#id) | guid |  
| [Name](Applications.AssetManagement.ManagedAssetGroups.md#name) | [MultilanguageString](../data-types.md#multilanguagestring) | Name of the asset group (multi-language). `Required` `Filter(eq;like)` 
| [Notes](Applications.AssetManagement.ManagedAssetGroups.md#notes) | string (max) __nullable__ | Notes for this ManagedAssetGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.AssetManagement.ManagedAssetGroups.md#parent) | [ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md) (nullable) | The parent asset group in the hierarchy. null means this is a root group. `Filter(multi eq)` |


## Attribute Details

### Code

Unique (within all groups) code of the asset group. `Required` `Filter(multi eq;like)` `ORD`

_Type_: **string (16)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  
_Maximum Length_: **16**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Name

Name of the asset group (multi-language). `Required` `Filter(eq;like)`

_Type_: **[MultilanguageString](../data-types.md#multilanguagestring)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

Notes for this ManagedAssetGroup.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Parent

The parent asset group in the hierarchy. null means this is a root group. `Filter(multi eq)`

_Type_: **[ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetGroups?$top=10>

