# Table Prj_Project_Work_Elements

Contains the work elements from the work breakdown structure, which are included in the projects. Entity: Prj_Project_Work_Elements

## Owner Tables Hierarchy

* [Prj_Projects](Prj_Projects.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Work_Element_Id](#project_work_element_id)|`uniqueidentifier` `PK`||
|[Project_Id](#project_id)|`uniqueidentifier` ||
|[Project_Type_Work_Element_Id](#project_type_work_element_id)|`uniqueidentifier` |The work element from the project type on which the current work element is based.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Id

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


