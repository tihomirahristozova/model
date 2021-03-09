# Table Prj_Template_Work_Elements

Contains project work elements, which shall be copied to projects, based on the specified template. Entity: Prj_Template_Work_Elements

## Owner Tables Hierarchy

* [Prj_Templates](Prj_Templates.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Template_Work_Element_Id](#project_template_work_element_id)|`uniqueidentifier` `PK`||
|[Project_Template_Id](#project_template_id)|`uniqueidentifier` ||
|[Project_Type_Work_Element_Id](#project_type_work_element_id)|`uniqueidentifier` |The work element from the project type, which shall be copied as work element in new projects, based on this template.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Template_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Template_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


