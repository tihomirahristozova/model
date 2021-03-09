# Table Prj_Project_Task_Materials

Contains the materials, which are required for a project task. Entity: Prj_Project_Task_Materials

## Owner Tables Hierarchy

* [Prj_Project_Tasks](Prj_Project_Tasks.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Task_Material_Id](#project_task_material_id)|`uniqueidentifier` `PK`||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The task for which is the material requirement|
|[Material_Product_Id](#material_product_id)|`uniqueidentifier` |The product Id of the required material|
|[Quantity](#quantity)|`decimal(9, 3)` |The required quantity of the material|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of the required quantity|
|[Line_Number](#line_number)|`int` |Line number within the task, increased in steps of 10. Used for sorting purposes|
|[Budgeted_Material_Amount](#budgeted_material_amount)|`decimal(12, 2)` |Budgeted amount for the material in the currency of the project. NULL means there is still no budgeted amount|
|[Quantity_Base](#quantity_base)|`decimal(9, 3)` Readonly|The equivalence of Quantity in the base measurement unit of the Material.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Task_Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Task_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Material_Product_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Line_Number

| Property | Value |
| - | - |
|Type|int|

### Budgeted_Material_Amount

| Property | Value |
| - | - |
|Type|decimal(12, 2)|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


