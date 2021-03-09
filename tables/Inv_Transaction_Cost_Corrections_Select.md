# Query Inv_Transaction_Cost_Corrections_Select


## Summary

| Name | Type | Description |
| - | - | --- |
|[Transaction_Id](#transaction_id)|`uniqueidentifier` |Unique Transaction Id|
|[Transaction_Line_Id](#transaction_line_id)|`uniqueidentifier` `PK`|The transaction line, which is corrected.|
|[Cost_Correction_Amount](#cost_correction_amount)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Amount field of the transaction line.|
|[Product_Cost_Adjustment](#product_cost_adjustment)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Product Cost field of the transaction line.|
|[Store_Cost_Adjustment](#store_cost_adjustment)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Store Cost field of the transaction line.|
|[Base_Cost_Adjustment](#base_cost_adjustment)|`decimal(0, 0)` |The amount of correction (plus or minus) for the Base Cost field of the transaction line.|

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
|Type|decimal(0, 0)|

### Product_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Store_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Base_Cost_Adjustment

| Property | Value |
| - | - |
|Type|decimal(0, 0)|


