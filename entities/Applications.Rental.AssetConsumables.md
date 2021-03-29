---
uid: Applications.Rental.AssetConsumables
---
# Applications.Rental.AssetConsumables Entity

**Namespace:** [Applications.Rental](Applications.Rental.md)  

Consumables are products, which are usually sold accompanying an asset rental. Entity: Rent_Asset_Consumables

## Default Visualization
Default Display Text Format:  
_{RentalAsset.RentalAssetCode}: {RentalAsset.RentalAssetName:T}_  
Default Search Member:  
_RentalAsset.RentalAssetCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[Applications.Rental.Assets](Applications.Rental.Assets.md)  
Aggregate Root:  
[Applications.Rental.AssetGroups](Applications.Rental.AssetGroups.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantity](Applications.Rental.AssetConsumables.md#consumablequantity) | [Quantity (12, 3)](../data-types.md#quantity) | Specifies what quantity of the consumable should be offered for each rented asset. `Unit: ConsumableQuantityUnit` `Required` 
| [Id](Applications.Rental.AssetConsumables.md#id) | guid |  
| [Notes](Applications.Rental.AssetConsumables.md#notes) | string (max) __nullable__ | Notes for this AssetConsumable. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [ConsumableQuantityUnit](Applications.Rental.AssetConsumables.md#consumablequantityunit) | [MeasurementUnits](General.MeasurementUnits.md) | The measurement unit of Consumable Quantity. `Required` `Filter(multi eq)` |
| [Product](Applications.Rental.AssetConsumables.md#product) | [Products](General.Products.Products.md) | The consumable which is offered accompanying the asset rental. `Required` `Filter(multi eq)` |
| [RentalAsset](Applications.Rental.AssetConsumables.md#rentalasset) | [Assets](Applications.Rental.Assets.md) | The rental asset for which the consumable would be offered. `Required` `Filter(multi eq)` `Owner` |
| [Store](Applications.Rental.AssetConsumables.md#store) | [Stores](Logistics.Inventory.Stores.md) | The store which contains the consumable. `Required` `Filter(multi eq)` |


## Attribute Details

### ConsumableQuantity

Specifies what quantity of the consumable should be offered for each rented asset. `Unit: ConsumableQuantityUnit` `Required`

_Type_: **[Quantity (12, 3)](../data-types.md#quantity)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this AssetConsumable.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### ConsumableQuantityUnit

The measurement unit of Consumable Quantity. `Required` `Filter(multi eq)`

_Type_: **[MeasurementUnits](General.MeasurementUnits.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Product

The consumable which is offered accompanying the asset rental. `Required` `Filter(multi eq)`

_Type_: **[Products](General.Products.Products.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### RentalAsset

The rental asset for which the consumable would be offered. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Assets](Applications.Rental.Assets.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### Store

The store which contains the consumable. `Required` `Filter(multi eq)`

_Type_: **[Stores](Logistics.Inventory.Stores.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Applications.Rental.AssetConsumables erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Applications.Rental.AssetConsumables erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Applications_Rental_AssetConsumables?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Applications_Rental_AssetConsumables?$top=10>

