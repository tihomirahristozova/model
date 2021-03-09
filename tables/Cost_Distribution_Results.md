# Table Cost_Distribution_Results

Contains the results of a cost distribution calculation. Entity: Cost_Distribution_Results

## Owner Tables Hierarchy

* [Cost_Distributions](Cost_Distributions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Distribution_Result_Id](#cost_distribution_result_id)|`uniqueidentifier` `PK`||
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Consecutive line number (within the cost distribution document) of the result.|
|[Output_Line_No](#output_line_no)|`int` |The line number (within the document) of the output over which the cost is distributed.|
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` |The cost type for which the current distribution is calculated.|
|[Distributed_Amount_Base](#distributed_amount_base)|`decimal(14, 5)` |The amount (in base currency) of the distributed cost. The amount is calculated for the combination of output and cost type.|

## Columns

### Cost_Distribution_Result_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Cost_Distribution_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Output_Line_No

| Property | Value |
| - | - |
|Type|int|

### Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Distributed_Amount_Base

| Property | Value |
| - | - |
|Type|decimal(14, 5)|


