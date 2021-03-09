# Query Cost_Distribution_Outputs_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Cost_Distribution_Output_Id](#cost_distribution_output_id)|`uniqueidentifier` `PK`||
|[Cost_Distribution_Id](#cost_distribution_id)|`uniqueidentifier` ||
|[Line_No](#line_no)|`int` |Unique, consecutive line number.|
|[Store_Transaction_Line_Id](#store_transaction_line_id)|`uniqueidentifier` |The store transaction line, for which costs will be distributed.|
|[Weight_Coefficient](#weight_coefficient)|`decimal(0, 0)` |The weight coefficient for prorate distribution of cost over the current line.|

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
|Type|decimal(0, 0)|


