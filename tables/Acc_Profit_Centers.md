# Table Acc_Profit_Centers

Defines company profit centers and their relative weight for automatic balance transfers from cost centers. Entity: Acc_Profit_Centers

## Summary

| Name | Type | Description |
| - | - | --- |
|[Profit_Center_Id](#profit_center_id)|`uniqueidentifier` `PK`||
|[Parent_Profit_Center_Id](#parent_profit_center_id)|`uniqueidentifier` |Parent profit center, NULL if this is root profit center|
|[Profit_Center_Name](#profit_center_name)|`nvarchar(254)` ||
|[Relative_Weight](#relative_weight)|`decimal(18, 4)` |The weight of this profit center, relative to the other profit centers within the same parent. The weight is used during profit distribution calculations. The sum of weights of all profit centers within a parent does not need to be 100, the ratio of total weight over weight is used.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Profit_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Profit_Center_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Profit_Center_Name

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

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


