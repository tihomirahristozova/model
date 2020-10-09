---
uid: Applications.Rental.AssetGroups
---
# Applications.Rental.AssetGroups Entity

Groups the rentable assets in hierarchy of logical groups. Entity: Rent_Asset_Groups

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [FullPath](Applications.Rental.AssetGroups.md#fullpath) | string (nullable) | The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. [ORD] [ReadOnly] 
| [Id](Applications.Rental.AssetGroups.md#id) | guid |  
| [Notes](Applications.Rental.AssetGroups.md#notes) | string (nullable) | Notes for this AssetGroup. 
| [ParentFullPath](Applications.Rental.AssetGroups.md#parentfullpath) | string (nullable) | The full path of the parent node. [Filter(eq)] 
| [RentalAssetGroupCode](Applications.Rental.AssetGroups.md#rentalassetgroupcode) | string | Asset group code, unique within the parent node. [Required] [Filter(eq;like)] 
| [RentalAssetGroupName](Applications.Rental.AssetGroups.md#rentalassetgroupname) | string | Asset group name, unique within the parent node. [Required] [Filter(eq;like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Assets | [Assets](Applications.Rental.Assets.md) | List of [Asset](Applications.Rental.Assets.md) child objects, based on the [Applications.Rental.Asset.RentalAssetGroup](Applications.Rental.Assets.md#rentalassetgroup) back reference 


## Attribute Details

### FullPath

The full path of the node in the format of dot-delimited, dot-terminated codes of the parents. [ORD] [ReadOnly]

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **True**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this AssetGroup.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### ParentFullPath

The full path of the parent node. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### RentalAssetGroupCode

Asset group code, unique within the parent node. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  

### RentalAssetGroupName

Asset group name, unique within the parent node. [Required] [Filter(eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Rental.AssetGroups erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.AssetGroups erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.AssetGroups erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetGroups?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetGroups?$top=10>

