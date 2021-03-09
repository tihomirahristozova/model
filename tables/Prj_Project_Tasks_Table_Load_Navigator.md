# Query Prj_Project_Tasks_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` ||
|[Project_Name](#project_name)|`nvarchar` ||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` ||
|[Project_Notes](#project_notes)|`nvarchar` ||
|[Start_Date](#start_date)|`date` ||
|[Finish_Date](#finish_date)|`date` ||
|[Project_Manager_Person_Id](#project_manager_person_id)|`uniqueidentifier` ||
|[Client_Party_Id](#client_party_id)|`uniqueidentifier` ||
|[Project_Status](#project_status)|`tinyint` Allowed: `0`, `10`, `20`, `30`, `40`, `45`, `50`, `55`||
|[Budgeting_Currency_Id](#budgeting_currency_id)|`uniqueidentifier` ||
|[Project_Code](#project_code)|`nvarchar` ||
|[Project_Type_Work_Element_Id](#project_type_work_element_id)|`uniqueidentifier` ||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` ||
|[Project_Work_Element_Id](#project_work_element_id)|`uniqueidentifier` ||
|[Task_Name](#task_name)|`nvarchar` ||
|[Notes](#notes)|`nvarchar` ||
|[Resource_Id](#resource_id)|`uniqueidentifier` ||
|[Start_Date_Time](#start_date_time)|`datetime` ||
|[Finish_Date_Time](#finish_date_time)|`datetime` ||
|[Planned_Duration_Hours](#planned_duration_hours)|`decimal(0, 0)` ||
|[Budget_Labor_Amount](#budget_labor_amount)|`decimal(0, 0)` ||
|[Responsible_Party_Id](#responsible_party_id)|`uniqueidentifier` ||
|[Activity_Id](#activity_id)|`uniqueidentifier` ||
|[Project_Task_No](#project_task_no)|`int` ||
|[Budgeted_Material_Amount](#budgeted_material_amount)|`decimal(0, 0)` ||
|[Budgeted_Billing_Amount](#budgeted_billing_amount)|`decimal(0, 0)` ||
|[Budgeted_Cost_Amount](#budgeted_cost_amount)|`decimal(0, 0)` ||
|[Work_Type_Id](#work_type_id)|`uniqueidentifier` |Type of work to be done. NULL means that type of work is undetermined yet.|
|[Task_Type_Id](#task_type_id)|`uniqueidentifier` |The type of the task. Determines the work type of the tasks, default billing rules, etc.|
|[Project_Type_Work_Element_Id_L1_Name](#project_type_work_element_id_l1_name)|`nvarchar` `ML`||
|[Project_Type_Work_Element_Id_L2_Name](#project_type_work_element_id_l2_name)|`nvarchar` `ML`||
|[Project_Type_Work_Element_Id_L3_Name](#project_type_work_element_id_l3_name)|`nvarchar` `ML`||
|[Project_Type_Work_Element_Id_L4_Name](#project_type_work_element_id_l4_name)|`nvarchar` `ML`||
|[Project_Type_Work_Element_Id_L5_Name](#project_type_work_element_id_l5_name)|`nvarchar` `ML`||
|[Project_Type_Work_Element_Id_L6_Name](#project_type_work_element_id_l6_name)|`nvarchar` `ML`||

## Columns

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

### Project_Notes

| Property | Value |
| - | - |
|Type|nvarchar|

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

### Project_Type_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_Id

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

### Notes

| Property | Value |
| - | - |
|Type|nvarchar|

### Resource_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Start_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

### Finish_Date_Time

| Property | Value |
| - | - |
|Type|datetime|

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

### Budgeted_Material_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Budgeted_Billing_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Budgeted_Cost_Amount

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Work_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Task_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Work_Element_Id_L1_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Work_Element_Id_L2_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Work_Element_Id_L3_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Work_Element_Id_L4_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Work_Element_Id_L5_Name

| Property | Value |
| - | - |
|Type|nvarchar|

### Project_Type_Work_Element_Id_L6_Name

| Property | Value |
| - | - |
|Type|nvarchar|


