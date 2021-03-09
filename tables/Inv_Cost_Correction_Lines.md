# Table Inv_Cost_Correction_Lines

Cost correction detail lines. One line is created for each corrected transaction line. Entity: Inv_Cost_Correction_Lines

## Owner Tables Hierarchy

* [Inv_Cost_Corrections](Inv_Cost_Corrections.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Correction_Line_Id](#cost_correction_line_id)|`uniqueidentifier` `PK`||
|[Cost_Correction_Id](#cost_correction_id)|`uniqueidentifier` ||
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` |The transaction line, which is corrected.|
|[Cost_Correction_Amount](#cost_correction_amount)|`decimal(14, 2)` |The amount of correction (plus or minus) for the Amount field of the transaction line.|
|[Product_Cost_Adjustment](#product_cost_adjustment)|`decimal(14, 2)` |The amount of correction (plus or minus) for the Product Cost field of the transaction line.|
|[Store_Cost_Adjustment](#store_cost_adjustment)|`decimal(14, 2)` |The amount of correction (plus or minus) for the Store Cost field of the transaction line.|
|[Base_Cost_Adjustment](#base_cost_adjustment)|`decimal(14, 2)` |The amount of correction (plus or minus) for the Base Cost field of the transaction line.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Correction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Correction_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Correction_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Product_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Store_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Base_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


