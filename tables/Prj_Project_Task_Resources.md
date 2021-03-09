# Table Prj_Project_Task_Resources

Contains the resources, required by the project tasks. Entity: Prj_Project_Task_Resources

## Owner Tables Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Resource_Id](#project_task_resource_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The task for which the resource is planned.|
|[Resource_Id](#resource_id)|`uniqueidentifier` |The planned resource.|
|[Resource_Usage_Percent](#resource_usage_percent)|`decimal(18, 4)` |The planned resource usage for this activity in percents. Values of more than 100% are allowed when more than 1 resource is required.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Resource_Usage_Hours](#resource_usage_hours)|`decimal(10, 2)` |The total number of resource-hours, which are planned for this task. Equals to the length of the task, multiplied by the resource usage.|
|[Cost_Per_Hour](#cost_per_hour)|`decimal(12, 5)` |Cost per hour for the resource usage for this task (in the currency of the project).|
|[Task_Total_Cost](#task_total_cost)|`decimal(14, 2)` |Total cost for this task (in the currency of the project).|
|[Billing_Price_Per_Hour](#billing_price_per_hour)|`decimal(12, 5)` |When not null, specifies the price per hour (in the currency of the Project) of resource usage which will be used for billing. NULL means that the item will be billed in another way. This way of billing is mutually exclusive with Fixed Total Price|
|[Billing_Total_Amount](#billing_total_amount)|`decimal(14, 2)` |When not NULL, specifies that this item will be billed for the specified fixed total price (in the currency of the Project). NULL means that this item will be billed in another way. This way of billing is mutually exclusive with Billing Price Per Hour.|
|[Per_Use_Cost](#per_use_cost)|`decimal(14, 2)` |One time cost for each resource usage, specified in the projects currency.|
|[Resource_Instance_Id](#resource_instance_id)|`uniqueidentifier` |The concrete resource instance, which should be used. NULL when no specific resource instance is required.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Task_Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Resource_Usage_Percent

| Property | Value |
| - | - |
|Type|decimal(18, 4)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Resource_Usage_Hours

| Property | Value |
| - | - |
|Type|decimal(10, 2)|

### Cost_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(12, 5)|

### Task_Total_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Billing_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(12, 5)|

### Billing_Total_Amount

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Per_Use_Cost

| Property | Value |
| - | - |
|Type|decimal(14, 2)|

### Resource_Instance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


