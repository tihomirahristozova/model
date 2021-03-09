# Query Prd_Resources_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`||
|[Resource_Group_Id](#resource_group_id)|`uniqueidentifier` ||
|[Resource_Name](#resource_name)|`nvarchar` ||
|[Primary_Unit_Id](#primary_unit_id)|`uniqueidentifier` ||
|[Setup_Scrap_Quantity](#setup_scrap_quantity)|`decimal(0, 0)` ||
|[Setup_Scrap_Unit](#setup_scrap_unit)|`uniqueidentifier` ||
|[Setup_Duration_Hours](#setup_duration_hours)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(0, 0)` |Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used.|
|[Resource_Currency_Id](#resource_currency_id)|`uniqueidentifier` |Currency for this resource. This currency applies for the standard price and cost per hour.|
|[Standard_Cost_Per_Hour](#standard_cost_per_hour)|`decimal(0, 0)` |Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Group_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Primary_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Setup_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Setup_Scrap_Unit

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Setup_Duration_Hours

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Standard_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Resource_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Cost_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


