# View Inv_Transaction_Cost_Corrections_Summary

Summary of cost corrections, grouped by the line corrected. Entity: Inv_Transaction_Cost_Corrections_Summary

## Owner Tables Hierarchy

* [Inv_Transactions](Inv_Transactions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Transaction_Id](#transaction_id)|`uniqueidentifier` ||
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` ||
|[Cost_Correction_Amount](#cost_correction_amount)|`decimal(38, 2)` |The cost correction in the original currency of the store transaction.|
|[Product_Cost_Adjustment](#product_cost_adjustment)|`decimal(38, 2)` |The cost correction in Products currency.|
|[Store_Cost_Adjustment](#store_cost_adjustment)|`decimal(38, 2)` |The cost correction in Stores currency.|
|[Base_Cost_Adjustment](#base_cost_adjustment)|`decimal(38, 2)` |The cost correction in Base currency.|

## Columns

### Transaction_Id

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
|Type|decimal(38, 2)|

### Product_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(38, 2)|

### Store_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(38, 2)|

### Base_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(38, 2)|


