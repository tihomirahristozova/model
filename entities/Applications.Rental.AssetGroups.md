---
uid: Applications.Rental.AssetGroups
---
# Applications.Rental.AssetGroups Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

Groups the rentable assets in hierarchy of logical groups. Entity: Rent_Asset_Groups

## Default Visualization
Default Display Text Format:  
_{RentalAssetGroupName}_  
Default Search Members:  
_RentalAssetGroupCode; RentalAssetGroupName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Rental.AssetGroups](Applications.Rental.AssetGroups.md)  
  * [Applications.Rental.Assets](Applications.Rental.Assets.md)  
    * [Applications.Rental.AssetConsumables](Applications.Rental.AssetConsumables.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Applications.Rental.AssetGroups.md#fullpath) | string (25) __nullable__ | The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. `ORD` `ReadOnly` 
| [Id](Applications.Rental.AssetGroups.md#id) | guid |  
| [Notes](Applications.Rental.AssetGroups.md#notes) | string (max) __nullable__ | Notes for this AssetGroup. 
| [ParentFullPath](Applications.Rental.AssetGroups.md#parentfullpath) | string (25) __nullable__ | The full path of the parent node. `Filter(eq)` 
| [RentalAssetGroupCode](Applications.Rental.AssetGroups.md#rentalassetgroupcode) | string (3) | Asset group code, unique within the parent node. `Required` `Filter(eq;like)` 
| [RentalAssetGroupName](Applications.Rental.AssetGroups.md#rentalassetgroupname) | string (254) | Asset group name, unique within the parent node. `Required` `Filter(eq;like)` 
| [RowVersion](Applications.Rental.AssetGroups.md#rowversion) | byte[] |  

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Assets | [Assets](Applications.Rental.Assets.md) | List of `Asset`(Applications.Rental.Assets.md) child objects, based on the `Applications.Rental.Asset.RentalAssetGroup`(Applications.Rental.Assets.md#rentalassetgroup) back reference 


## Attribute Details

### FullPath

The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. `ORD` `ReadOnly`

_Type_: **string (25) __nullable__**  
_Indexed_: **True**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  
_Maximum Length_: **25**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this AssetGroup.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### ParentFullPath

The full path of the parent node. `Filter(eq)`

_Type_: **string (25) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **25**  

### RentalAssetGroupCode

Asset group code, unique within the parent node. `Required` `Filter(eq;like)`

_Type_: **string (3)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **3**  

### RentalAssetGroupName

Asset group name, unique within the parent node. `Required` `Filter(eq;like)`

_Type_: **string (254)**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### RowVersion

_Type_: **byte[]**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  



## Business Rules

[!list limit=1000 erp.entity=Applications.Rental.AssetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Applications.Rental.AssetGroups erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetGroups?$top=10>

