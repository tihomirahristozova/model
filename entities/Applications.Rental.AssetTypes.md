# Applications.Rental.AssetTypes

Categorizes the rental assets in specific type categories. Entity: Rent_Asset_Types

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Applications.Rental.AssetTypes.md#Id) | guid |  
| [Notes](Applications.Rental.AssetTypes.md#Notes) | string (nullable) | Notes for this AssetType. [Filter(like)] 
| [RentalAssetTypeName](Applications.Rental.AssetTypes.md#RentalAssetTypeName) | string | The name of the rental asset type. [Required] [Filter(like)] 

## Child Collections

| Name | Type | Description |
| ---- | ---- | --- |
| Consumables | [Applications.Rental.AssetTypeConsumables](Applications.Rental.AssetTypeConsumables.md) | List of [AssetTypeConsumable](Applications.Rental.AssetTypeConsumables.md) child objects, based on the [Applications.Rental.AssetTypeConsumable.RentalAssetType](Applications.Rental.AssetTypeConsumables.md#RentalAssetType) back reference 
| AssetTypeProperties | [Applications.Rental.AssetTypeProperties](Applications.Rental.AssetTypeProperties.md) | List of [AssetTypeProperty](Applications.Rental.AssetTypeProperties.md) child objects, based on the [Applications.Rental.AssetTypeProperty.RentalAssetType](Applications.Rental.AssetTypeProperties.md#RentalAssetType) back reference 


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Supports Order By_: **False**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this AssetType. [Filter(like)]

_Type_: **string (nullable)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  

### RentalAssetTypeName

> The name of the rental asset type. [Required] [Filter(like)]

_Type_: **string**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  



## Business Rules

[!list erp.entity=Applications.Rental.AssetTypes erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.AssetTypes erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.AssetTypes erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetTypes?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetTypes?$top=10>

Table API Query:
<https://demodb.my.erp.net/api/domain/odata/Rent_Asset_Types?$top=10>

