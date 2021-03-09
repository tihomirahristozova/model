# Table Cost_Distribution_Costs

The cost types and their amounts which are distributed by a Cost Distribution document. Entity: Cost_Distribution_Costs

## Owner Tables Hierarchy

* [Cost_Distributions](Cost_Distributions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Distribution_Cost_Id](#cost_distribution_cost_id)|`uniqueidentifier` `PK`||
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` ||
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` |The type of the cost, which will be distributed.|
|[Amount_Base](#amount_base)|`decimal(12, 2)` |The cost (in base currency) which should be distributed.|
|[Notes](#notes)|`nvarchar(2147483647)` ||

## Columns

### Cost_Distribution_Cost_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Distribution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Base

| Property | Value |
| - | - |
|Type|decimal(12, 2)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|


