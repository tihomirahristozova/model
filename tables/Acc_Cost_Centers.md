# Table Acc_Cost_Centers

Defines cost centers and their relation to profit centers. Entity: Acc_Cost_Centers

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Center_Id](#cost_center_id)|`uniqueidentifier` `PK`||
|[Parent_Cost_Center_Id](#parent_cost_center_id)|`uniqueidentifier` |Parent cost center, NULL if this is root cost center|
|[Cost_Center_Name](#cost_center_name)|`nvarchar(254)` ||
|[Relative_Weight](#relative_weight)|`decimal(18, 4)` |The weight of this cost center, relative to the other cost centers within the same parent. The weight is used during cost distribution calculations. The sum of weights of all cost centers within a parent does not need to be 100, the ratio of total weight over weight is used.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Transfer_Cost_To_Profit_Center_Id](#transfer_cost_to_profit_center_id)|`uniqueidentifier` |Points to the profit center to which to transfer the cost. Valid only for leaf cost centers|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Cost_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Center_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Relative_Weight

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Transfer_Cost_To_Profit_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


