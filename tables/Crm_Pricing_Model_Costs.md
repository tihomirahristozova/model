# Table Crm_Pricing_Model_Costs

List of costs, associated with a pricing model. Entity: Crm_Pricing_Model_Costs

## Owner Tables Hierarchy

* [Crm_Pricing_Models](Crm_Pricing_Models.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Pricing_Model_Cost_Id](#pricing_model_cost_id)|`uniqueidentifier` `PK`|Pricing Model Cost|
|[Pricing_Model_Id](#pricing_model_id)|`uniqueidentifier` |Pricing model, for which the cost is defined|
|[Line_No](#line_no)|`int` |The consequtive number of the cost within the pricing model|
|[Cost_Type_Id](#cost_type_id)|`uniqueidentifier` |The cost type, which is listed for the pricing model|
|[Amount_Percent](#amount_percent)|`decimal(6, 5)` |Used when the cost is calculated as percent of the amount. NULL when the cost is calculated in a different way|
|[Amount_Per_Unit](#amount_per_unit)|`decimal(9, 2)` |Used when the cost is calculated as amount per unit of the product. The unit is defined in Measurement_Unit_Id. NULL when the cost is calculated in a different way|
|[Measurement_Unit_Id](#measurement_unit_id)|`uniqueidentifier` |The measurement unit for which the Amount_Per_Unit is defined. NULL when the cost is calculated in a different way|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Pricing_Model_Cost_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Pricing_Model_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_No

| Property | Value |
| - | - |
|Type|int|

### Cost_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Amount_Percent

| Property | Value |
| - | - |
|Type|decimal(6, 5)|

### Amount_Per_Unit

| Property | Value |
| - | - |
|Type|decimal(9, 2)|

### Measurement_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


