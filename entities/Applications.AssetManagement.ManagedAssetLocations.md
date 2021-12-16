---
uid: Applications.AssetManagement.ManagedAssetLocations
---
# Applications.AssetManagement.ManagedAssetLocations Entity

**Namespace:** [Applications.AssetManagement](Applications.AssetManagement.md)  

Contains the locations to which the assets are assigned at various moments in time. Entity: Eam_Managed_Asset_Locations (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{ManagedAsset.Name:T}_  
Default Search Members:  
_ManagedAsset.Name_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.AssetManagement.ManagedAssets](Applications.AssetManagement.ManagedAssets.md)  
Aggregate Root:  
[Applications.AssetManagement.ManagedAssets](Applications.AssetManagement.ManagedAssets.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FromDate](Applications.AssetManagement.ManagedAssetLocations.md#fromdate) | date | The date on which the asset is assigned to the location. `Required` `Default(Now)` 
| [Id](Applications.AssetManagement.ManagedAssetLocations.md#id) | guid |  
| [Notes](Applications.AssetManagement.ManagedAssetLocations.md#notes) | string (max) __nullable__ | Might contain additional notes for the exact location of the asset within the enterprise company location. 
| [RowVersion](Applications.AssetManagement.ManagedAssetLocations.md#rowversion) | byte[] |  

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompanyLocation](Applications.AssetManagement.ManagedAssetLocations.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) | The enterprise company location, where the asset is assigned. `Required` `Filter(multi eq)` |
| [ManagedAsset](Applications.AssetManagement.ManagedAssetLocations.md#managedasset) | [ManagedAssets](Applications.AssetManagement.ManagedAssets.md) | The asset, whose location is recorded. `Required` `Filter(multi eq)` `Owner` |
| [ResponsiblePerson](Applications.AssetManagement.ManagedAssetLocations.md#responsibleperson) | [Persons](General.Contacts.Persons.md) (nullable) | The responsible person, to which the asset is assigned. null when the asset is not assigned to any particular responsible person. `Filter(multi eq)` |


## Attribute Details

### FromDate

The date on which the asset is assigned to the location. `Required` `Default(Now)`

_Type_: **date**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Default Value_: **CurrentDateTime**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Might contain additional notes for the exact location of the asset within the enterprise company location.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompanyLocation

The enterprise company location, where the asset is assigned. `Required` `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### ManagedAsset

The asset, whose location is recorded. `Required` `Filter(multi eq)` `Owner`

_Type_: **[ManagedAssets](Applications.AssetManagement.ManagedAssets.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### ResponsiblePerson

The responsible person, to which the asset is assigned. null when the asset is not assigned to any particular responsible person. `Filter(multi eq)`

_Type_: **[Persons](General.Contacts.Persons.md) (nullable)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetLocations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.AssetManagement.ManagedAssetLocations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_AssetManagement_ManagedAssetLocations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_AssetManagement_ManagedAssetLocations?$top=10>

