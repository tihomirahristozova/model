# Table Prd_Resources

Resource types available to production. Entity: Prd_Resources

## Owner Tables Hierarchy

* [Prd_Resource_Groups](Prd_Resource_Groups.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Id](#id)|`uniqueidentifier` `PK`|Unique resource id|
|[Resource_Group_Id](#resource_group_id)|`uniqueidentifier` |The Id of the containing resource group|
|[Resource_Name](#resource_name)|`nvarchar(64)` |Name of the resource|
|[Primary_Unit_Id](#primary_unit_id)|`uniqueidentifier` |Primary measurement unit for quantities of the resource|
|[Setup_Scrap_Quantity](#setup_scrap_quantity)|`decimal(18, 3)` |The usual quantity of fixed scrap occurring when changing production. |
|[Setup_Scrap_Unit](#setup_scrap_unit)|`uniqueidentifier` |The measurement units of Setup_Scrap_Quantity|
|[Setup_Duration_Hours](#setup_duration_hours)|`decimal(6, 2)` |The usual duration of setup when changing production|
|[Notes](#notes)|`nvarchar(254)` |User notes for the resource|
|[Standard_Price_Per_Hour](#standard_price_per_hour)|`decimal(18, 6)` |Standard price per hour for this resource. It participates in the calculation of standard price for production recipes in which the current resource is used.|
|[Resource_Currency_Id](#resource_currency_id)|`uniqueidentifier` |Currency for this resource. This currency applies for the standard price and cost per hour.|
|[Standard_Cost_Per_Hour](#standard_cost_per_hour)|`decimal(18, 6)` |Standard cost per hour for this resource. It participates in the calculation of standard cost for production recipes in which the current resource is used.|
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
|Type|nvarchar(64)|

### Primary_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Setup_Scrap_Quantity

| Property | Value |
| - | - |
|Type|decimal(18, 3)|

### Setup_Scrap_Unit

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Setup_Duration_Hours

| Property | Value |
| - | - |
|Type|decimal(6, 2)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Standard_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Resource_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Standard_Cost_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(18, 6)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


