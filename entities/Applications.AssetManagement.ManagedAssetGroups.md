# Applications.AssetManagement.ManagedAssetGroups

Organizational hierarchy of asset groups. Entity: Eam_Managed_Asset_Groups (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.AssetManagement.ManagedAssetGroups.md#Id) | guid |  
| [Code](Applications.AssetManagement.ManagedAssetGroups.md#Code) | string | Unique (within all groups) code of the asset group. [Required] [Filter(multi eq;like)] [ORD] 
| [Name](Applications.AssetManagement.ManagedAssetGroups.md#Name) | [MultilanguageString](../data-types/MultilanguageString.md) | Name of the asset group (multi-language). [Required] [Filter(eq;like)] 
| [Notes](Applications.AssetManagement.ManagedAssetGroups.md#Notes) | string (nullable) | Notes for this ManagedAssetGroup. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Parent](Applications.AssetManagement.ManagedAssetGroups.md#Parent) | [Applications.AssetManagement.ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md) (nullable) | The parent asset group in the hierarchy. null means this is a root group. [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Code

> Unique (within all groups) code of the asset group. [Required] [Filter(multi eq;like)] [ORD]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **True**  

### Name

> Name of the asset group (multi-language). [Required] [Filter(eq;like)]

_Type_: **[MultilanguageString](../data-types/MultilanguageString.md)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### Notes

> Notes for this ManagedAssetGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Parent

> The parent asset group in the hierarchy. null means this is a root group. [Filter(multi eq)]

_Type_: **[Applications.AssetManagement.ManagedAssetGroups](Applications.AssetManagement.ManagedAssetGroups.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  



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

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Eam_Managed_Asset_Groups?$top=10>

