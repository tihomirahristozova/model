# Table Rent_Asset_Consumables

Consumables are products, which are usually sold accompanying an asset rental. Entity: Rent_Asset_Consumables

## Owner Tables Hierarchy

* [Rent_Assets](Rent_Assets.md)
* [Rent_Asset_Groups](Rent_Asset_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Asset_Consumable_Id](#asset_consumable_id)|`uniqueidentifier` `PK`||
|[Rental_Asset_Id](#rental_asset_id)|`uniqueidentifier` |The rental asset for which the consumable would be offered.|
|[Product_Id](#product_id)|`uniqueidentifier` |The consumable which is offered accompanying the asset rental.|
|[Consumable_Quantity](#consumable_quantity)|`decimal(12, 3)` |Specifies what quantity of the consumable should be offered for each rented asset.|
|[Consumable_Quantity_Unit_Id](#consumable_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Consumable Quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |The store which contains the consumable.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Asset_Consumable_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Rental_Asset_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Consumable_Quantity

| Property | Value |
| - | - |
|Type|decimal(12, 3)|

### Consumable_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Store_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


