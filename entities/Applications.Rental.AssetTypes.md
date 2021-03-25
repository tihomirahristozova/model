---
uid: Applications.Rental.AssetTypes
---
# Applications.Rental.AssetTypes Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

Categorizes the rental assets in specific type categories. Entity: Rent_Asset_Types

## Default Visualization
Default Display Text Format:  
_{RentalAssetTypeName:T}_  
Default Search Member:  
_RentalAssetTypeName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Applications.Rental.AssetTypes](Applications.Rental.AssetTypes.md)  
  * [Applications.Rental.AssetTypeConsumables](Applications.Rental.AssetTypeConsumables.md)  
  * [Applications.Rental.AssetTypeProperties](Applications.Rental.AssetTypeProperties.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.AssetTypes.md#id) | guid |  
| [Notes](Applications.Rental.AssetTypes.md#notes) | string (max) __nullable__ | Notes for this AssetType. `Filter(like)` 
| [RentalAssetTypeName](Applications.Rental.AssetTypes.md#rentalassettypename) | string (254) | The name of the rental asset type. `Required` `Filter(like)` 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| AssetTypeProperties | [AssetTypeProperties](Applications.Rental.AssetTypeProperties.md) | List of `AssetTypeProperty`(Applications.Rental.AssetTypeProperties.md) child objects, based on the `Applications.Rental.AssetTypeProperty.RentalAssetType`(Applications.Rental.AssetTypeProperties.md#rentalassettype) back reference 
| Consumables | [AssetTypeConsumables](Applications.Rental.AssetTypeConsumables.md) | List of `AssetTypeConsumable`(Applications.Rental.AssetTypeConsumables.md) child objects, based on the `Applications.Rental.AssetTypeConsumable.RentalAssetType`(Applications.Rental.AssetTypeConsumables.md#rentalassettype) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this AssetType. `Filter(like)`

_Type_: **string (max) __nullable__**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  

### RentalAssetTypeName

The name of the rental asset type. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  



## Business Rules

[!list erp.entity=Applications.Rental.AssetTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.AssetTypes erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetTypes?$top=10>

