# Query Gen_Product_Dimensions_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Source_Quantity_Unit_Id](#source_quantity_unit_id)|`uniqueidentifier` |The non-base measurement unit for which we specify convertion ratio|
|[Dest_Quantity_Unit_Id](#dest_quantity_unit_id)|`uniqueidentifier` |The measurement unit of Dest_Quantity. Should be one of the units of the base measurement category of the product|
|[Product_Dimension_Id](#product_dimension_id)|`uniqueidentifier` `PK`||
|[Product_Id](#product_id)|`uniqueidentifier` ||
|[Source_Quantity](#source_quantity)|`decimal(0, 0)` |The quantity in the non-base unit|
|[Measurement_Category_Id](#measurement_category_id)|`uniqueidentifier` Readonly|The measurement category of Source Quantity Unit. For each product, only one conversion ratio can be specified for a measurement category.|
|[Dest_Quantity](#dest_quantity)|`decimal(0, 0)` |Quantity in some of the base units, that equals Source_Quantity|
|[Convert_To_Base_Multiplier](#convert_to_base_multiplier)|`decimal(0, 0)` |This was intended to be the multiplier, but due to a historical bug actually contains the divisor of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system.|
|[Convert_To_Base_Divisor](#convert_to_base_divisor)|`decimal(0, 0)` |This was intended to be the divisor, but due to a historical bug actually contains the multiplier of the convertion ratio from the non-base measurement category to the base measurement category. This should be automatically calculated by the system.|

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
|Type|decimal(0, 0)|

### Measurement_Category_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Dest_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Convert_To_Base_Multiplier

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Convert_To_Base_Divisor

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


