# Table Gen_Product_Dimensions

Contains convertion ratios between the supported measument categories for each product. Does not contain a record for the default category of the products, for which the convertion ratio is defined as equal to 1. Entity: Gen_Product_Dimensions

## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Source_Quantity_Unit_Id](#source_quantity_unit_id)|`uniqueidentifier` |The non-base measurement unit for which we specify convertion ratio|
|[Dest_Quantity_Unit_Id](#dest_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Dest_Quantity. Should be one of the units of the base measurement category of the product|
|[Product_Dimension_Id](#product_dimension_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` |The product for which we specify conversion ratios|
|[Source_Quantity](#source_quantity)|`decimal(9, 3)` |The quantity in the non-base unit|
|[Measurement_Category_Id](#measurement_category_id)|`uniqueidentifier` Readonly|The measurement category of Source Quantity Unit. For each product, only one conversion ratio can be specified for a measurement category.|
|[Dest_Quantity](#dest_quantity)|`decimal(9, 3)` |Quantity in some of the base units, that equals Source_Quantity|
|[Convert_To_Base_Multiplier](#convert_to_base_multiplier)|`decimal(9, 3)` |This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system.|
|[Convert_To_Base_Divisor](#convert_to_base_divisor)|`decimal(9, 3)` |This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Source_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dest_Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Dimension_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Source_Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dest_Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Convert_To_Base_Multiplier

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Convert_To_Base_Divisor

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


