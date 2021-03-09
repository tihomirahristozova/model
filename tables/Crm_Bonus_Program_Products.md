# Table Crm_Bonus_Program_Products

Provides a way to specify additional (to the one specified in Bonus Program.Conditional Product) products, which will be used to evaluate bonus program conditions. When any of the products exists in the sales document, the conditions are satisfied and the program is applied. When the conditional products list for a bonus program is empty, it is considered that the program is valid for all products. Entity: Crm_Bonus_Program_Products

## Owner Tables Hierarchy

* [Crm_Bonus_Programs](Crm_Bonus_Programs.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Bonus_Program_Product_Id](#bonus_program_product_id)|`uniqueidentifier` `PK`||
|[Bonus_Program_Id](#bonus_program_id)|`uniqueidentifier` ||
|[Product_Id](#product_id)|`uniqueidentifier` |The product which is required to exist in the final sales document in order for the bonus program to be applied|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Bonus_Program_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Bonus_Program_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


