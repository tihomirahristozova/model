# Query Crm_Line_Discounts_Table_Look_Up


## Summary

| Name | Type | Description |
| - | - | --- |
|[Line_Discount_Id](#line_discount_id)|`uniqueidentifier` `PK`||
|[Description](#description)|`nvarchar` |The description of the discount that is shown to the operator when he/she should choose between different discounts|
|[Discount_Percent](#discount_percent)|`decimal(7, 6)` |The discount percent that should be applied if all the matching criteria are met.|
|[Priority](#priority)|`tinyint` Allowed: `1`, `2`, `3`, `4`, `5`|The priority of this discount policy. When selecting a discount for a sales document line, only the highest priority policy, matching the criteria is applied.|

## Columns

### Line_Discount_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Description

| Property | Value |
| - | - |
|Type|nvarchar|

### Discount_Percent

| Property | Value |
| - | - |
|Type|decimal(7, 6)|

### Priority

| Property | Value |
| - | - |
|Type|tinyint|


