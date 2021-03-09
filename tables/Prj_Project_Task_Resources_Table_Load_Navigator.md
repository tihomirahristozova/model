# Query Prj_Project_Task_Resources_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Resource_Id](#project_task_resource_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` ||
|[Resource_Id](#resource_id)|`uniqueidentifier` ||
|[Resource_Usage_Percent](#resource_usage_percent)|`decimal(0, 0)` ||
|[Notes](#notes)|`nvarchar` ||
|[Resource_Usage_Hours](#resource_usage_hours)|`decimal(0, 0)` ||
|[Cost_Per_Hour](#cost_per_hour)|`decimal(0, 0)` ||
|[Task_Total_Cost](#task_total_cost)|`decimal(0, 0)` ||
|[Billing_Price_Per_Hour](#billing_price_per_hour)|`decimal(0, 0)` ||
|[Billing_Total_Amount](#billing_total_amount)|`decimal(0, 0)` ||
|[Per_Use_Cost](#per_use_cost)|`decimal(0, 0)` ||
|[Resource_Instance_Id](#resource_instance_id)|`uniqueidentifier` |The concrete resource instance, which should be used. NULL when no specific resource instance is required.|
|[Project_Id](#project_id)|`uniqueidentifier` ||
|[Project_Work_Element_Id](#project_work_element_id)|`uniqueidentifier` ||
|[Task_Name](#task_name)|`nvarchar` ||
|[Start_Date_Time](#start_date_time)|`datetime` ||
|[Finish_Date_Time](#finish_date_time)|`datetime` ||
|[Work_Type_Id](#work_type_id)|`uniqueidentifier` ||
|[Planned_Duration_Hours](#planned_duration_hours)|`decimal(0, 0)` ||
|[Budget_Labor_Amount](#budget_labor_amount)|`decimal(0, 0)` ||
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` ||
|[Activity_Id](#activity_id)|`uniqueidentifier` ||
|[Project_Task_No](#project_task_no)|`int` ||
|[Task_Type_Id](#task_type_id)|`uniqueidentifier` |The type of the task. Determines the work type of the tasks, default billing rules, etc.|
|[Total_Price](#total_price)|`decimal(0, 0)` ||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Project_Name](#project_name)|`nvarchar` ||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` ||
|[Start_Date](#start_date)|`date` ||
|[Finish_Date](#finish_date)|`date` ||
|[Project_Manager_Person_Id](#project_manager_person_id)|`uniqueidentifier` ||
|[Client_Party_Id](#client_party_id)|`uniqueidentifier` ||
|[Project_Status](#project_status)|`tinyint` Allowed: `0`, `10`, `20`, `30`, `40`, `45`, `50`, `55`||
|[Budgeting_Currency_Id](#budgeting_currency_id)|`uniqueidentifier` ||
|[Project_Code](#project_code)|`nvarchar` ||

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
|Type|decimal(0, 0)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Resource_Usage_Hours

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Cost_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Task_Total_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Billing_Price_Per_Hour

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Billing_Total_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Per_Use_Cost

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Resource_Instance_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Task_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Finish_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Work_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Planned_Duration_Hours

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Budget_Labor_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Responsible_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Activity_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_No

| Property | Value |
| - | - |
|Type|int|

### Task_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Total_Price

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date

| Property | Value |
| - | - |
|Type|date|

### Finish_Date

| Property | Value |
| - | - |
|Type|date|

### Project_Manager_Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Client_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Status

| Property | Value |
| - | - |
|Type|tinyint|

### Budgeting_Currency_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Code

| Property | Value |
| - | - |
|Type|nvarchar|


