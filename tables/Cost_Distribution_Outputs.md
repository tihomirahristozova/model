# Table Cost_Distribution_Outputs

Contains the output data for the specified period. This is the output on which cost is distributed. Entity: Cost_Distribution_Outputs

## Owner Tables Hierarchy

* [Cost_Distributions](Cost_Distributions.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Distribution_Output_Id](#cost_distribution_output_id)|`uniqueidentifier` `PK`||
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Unique (within the document), consecutive line number of the output.|
|[Store_Transaction_Line_Id](#store_transaction_line_id)|`uniqueidentifier` |The store transaction line, for which costs will be distributed.|
|[Weight_Coefficient](#weight_coefficient)|`decimal(12, 5)` |The weight coefficient for prorate distribution of cost over the current line.|

## Columns

### Cost_Distribution_Output_Id

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

### Store_Transaction_Line_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Weight_Coefficient

| Property | Value |
| - | - |
|Type|decimal(12, 5)|


