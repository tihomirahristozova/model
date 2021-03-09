# Table Rent_Lease_Contract_Line_Consumables

Contains the consumables, which are sold accompanying asset rentals. Entity: Rent_Lease_Contract_Line_Consumables

## Owner Tables Hierarchy

* [Rent_Lease_Contract_Lines](Rent_Lease_Contract_Lines.md)
* [Rent_Lease_Contracts](Rent_Lease_Contracts.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Lease_Line_Consumable_Id](#lease_line_consumable_id)|`uniqueidentifier` `PK`||
|[Lease_Line_Id](#lease_line_id)|`uniqueidentifier` |Lease line with which the current consumable is given.|
|[Product_Id](#product_id)|`uniqueidentifier` |The consumable to be sold accompanying the asset.|
|[Consumable_Quantity](#consumable_quantity)|`decimal(12, 3)` |The quantity sold of the consumable.|
|[Consumable_Quantity_Unit_Id](#consumable_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Consumable Quantity.|
|[Store_Id](#store_id)|`uniqueidentifier` |Store from which the consumable is issued.|
|[Line_No](#line_no)|`int` |Consecutive number of the consumable within the lease contract line.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Lease_Line_Consumable_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Lease_Line_Id

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

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


