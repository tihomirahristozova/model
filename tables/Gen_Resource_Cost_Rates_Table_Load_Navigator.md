# Query Gen_Resource_Cost_Rates_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Resource_Cost_Rate_Id](#resource_cost_rate_id)|`uniqueidentifier` `PK`||
|[Resource_Id](#resource_id)|`uniqueidentifier` |The resource for which the cost rate is defined.|
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |The enterprise company for which the cost is defined.|
|[From_Date](#from_date)|`date` |Starting date of validity of the cost rate. The rate is valid until the next cost rate record with later date is defined.|
|[Standard_Rate_Per_Hour](#standard_rate_per_hour)|`decimal(12, 4)` |The standard cost per hour of the resource in the resources costing currency. The standard cost is applied for resource usage during the normal working hours.|
|[Overtime_Rate_Per_Hour](#overtime_rate_per_hour)|`decimal(12, 4)` |The overtime cost of the resource per hour in the resources costing currency. The overtime rate specifies the cost of the resource, when it is used outside the normal working schedule. NULL means that there is no special overtime rate and the standard rate should be applied.|
|[Per_Use_Cost](#per_use_cost)|`decimal(12, 2)` |One-time cost for each usage of the resource in the resources costing currency.|
|[Notes](#notes)|`nvarchar` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Resource_Cost_Rate_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### From_Date

| Property | Value |
| - | - |
|Type|date|

### Standard_Rate_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(12, 4)|

### Overtime_Rate_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(12, 4)|

### Per_Use_Cost

| Property | Value |
| - | - |
|Type|decimal(12, 2)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


