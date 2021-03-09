# Table Prj_Work_Report_Materials

Each record contains a consumed material, reported by the related Work Report. Entity: Prj_Work_Report_Materials

## Owner Tables Hierarchy

* [Prj_Work_Reports](Prj_Work_Reports.md)
* [Gen_Documents](Gen_Documents.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Work_Report_Material_Id](#work_report_material_id)|`uniqueidentifier` `PK`||
|[Work_Report_Id](#work_report_id)|`uniqueidentifier` ||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the materials are reported.|
|[Material_Product_Id](#material_product_id)|`uniqueidentifier` |The consumed material.|
|[Quantity](#quantity)|`decimal(9, 3)` |The consumed quantity of the material.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. It is strongly suggested that the same unit is used for planning and usage reporting.|
|[Quantity_Base](#quantity_base)|`decimal(9, 3)` Readonly|The equivalence of Quantity in the base measurement unit of the Material.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Work_Report_Material_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Work_Report_Id

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

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(9, 3)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


