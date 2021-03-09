# Table Prd_Product_Low_Levels


## Owner Tables Hierarchy

* [Gen_Products](Gen_Products.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Product_Id](#product_id)|`uniqueidentifier` `PK`|The product whose low level is recorded.|
|[Low_Level](#low_level)|`int` |The lowest level in the production tree, where this product is used as ingredient. 0 for products, that are not ingredients|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Low_Level

| Property | Value |
| - | - |
|Type|int|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


