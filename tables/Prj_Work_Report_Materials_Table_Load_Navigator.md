# Query Prj_Work_Report_Materials_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Work_Report_Material_Id](#work_report_material_id)|`uniqueidentifier` `PK`||
|[Work_Report_Id](#work_report_id)|`uniqueidentifier` ||
|[Project_Task_Id](#project_task_id)|`uniqueidentifier` |The project task for which the materials are reported.|
|[Material_Product_Id](#material_product_id)|`uniqueidentifier` |The consumed material.|
|[Quantity](#quantity)|`decimal(0, 0)` |The consumed quantity of the material.|
|[Quantity_Unit_Id](#quantity_unit_id)|`uniqueidentifier` |The measurement unit of Quantity. It is strongly suggested that the same unit is used for planning and usage reporting.|
|[Quantity_Base](#quantity_base)|`decimal(0, 0)` |The equivalence of Quantity in the base measurement unit of the Material.|
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
|Type|decimal(0, 0)|

### Quantity_Unit_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Quantity_Base

| Property | Value |
| - | - |
|Type|decimal(0, 0)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


