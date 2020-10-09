---
uid: Applications.Rental.AssetTypeConsumables
---
# Applications.Rental.AssetTypeConsumables Entity

Consumables are products, which are usually sold accompanying an asset rental. Entity: Rent_Asset_Type_Consumables

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantity](Applications.Rental.AssetTypeConsumables.md#consumablequantity) | [Quantity](../data-types.md#quantity) | Specifies what quantity of the consumable should be offered for each rented asset. [Unit: ConsumableQuantityUnit] [Required] 
| [Id](Applications.Rental.AssetTypeConsumables.md#id) | guid |  
| [Notes](Applications.Rental.AssetTypeConsumables.md#notes) | string (nullable) | Notes for this AssetTypeConsumable. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantityUnit](Applications.Rental.AssetTypeConsumables.md#consumablequantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Consumable Quantity. [Required] [Filter(multi eq)] |
| [Product](Applications.Rental.AssetTypeConsumables.md#product) | [Products](General.Products.Products.md) | The consumable which is offered accompanying the asset rental. [Required] [Filter(multi eq)] |
| [RentalAssetType](Applications.Rental.AssetTypeConsumables.md#rentalassettype) | [AssetTypes](Applications.Rental.AssetTypes.md) | The rental asset type for which the consumable would be offered. [Required] [Filter(multi eq)] [Owner] |
| [Store](Applications.Rental.AssetTypeConsumables.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store which contains the consumable. [Required] [Filter(multi eq)] |


## Attribute Details

### ConsumableQuantity

> Specifies what quantity of the consumable should be offered for each rented asset. [Unit: ConsumableQuantityUnit] [Required]

_Type_: **[Quantity](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this AssetTypeConsumable.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### ConsumableQuantityUnit

> The measurement unit of Consumable Quantity. [Required] [Filter(multi eq)]

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

> The consumable which is offered accompanying the asset rental. [Required] [Filter(multi eq)]

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RentalAssetType

> The rental asset type for which the consumable would be offered. [Required] [Filter(multi eq)] [Owner]

_Type_: **[AssetTypes](Applications.Rental.AssetTypes.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

> The store which contains the consumable. [Required] [Filter(multi eq)]

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Rental.AssetTypeConsumables erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.AssetTypeConsumables erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Applications.Rental.AssetTypeConsumables erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetTypeConsumables?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetTypeConsumables?$top=10>

