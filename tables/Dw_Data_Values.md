# Table Dw_Data_Values

The actual values in the general data warehouse. Entity: Dw_Data_Values (Introduced in version 18.2)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Data_Value_Id](#data_value_id)|`uniqueidentifier` `PK`||
|[Data_Measure_Id](#data_measure_id)|`uniqueidentifier` |The measure for which the data is recorded.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The Enterprise Company for which the data is recorded.|
|[Date](#date)|`date` |The date for which the measure is recorded. All records with dates within each period are summed.|
|[Target_Value](#target_value)|`decimal(17, 5)` |Accumulates target value for the measure.|
|[Actual_Value](#actual_value)|`decimal(17, 5)` |Accumulates actual value for the measure.|

## Columns

### Data_Value_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Data_Measure_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Date

| Property | Value |
| - | - |
|Type|date|

### Target_Value

| Property | Value |
| - | - |
|Type|decimal(17, 5)|

### Actual_Value

| Property | Value |
| - | - |
|Type|decimal(17, 5)|


