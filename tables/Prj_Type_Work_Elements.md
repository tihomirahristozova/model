# Table Prj_Type_Work_Elements

The work elements of the work breakdown structure of each project type. Entity: Prj_Type_Work_Elements

## Owner Tables Hierarchy

* [Prj_Types](Prj_Types.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Type_Work_Element_Id](#project_type_work_element_id)|`uniqueidentifier` `PK`||
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` ||
|[Parent_Full_Path](#parent_full_path)|`nvarchar(25)` |The full path of the parent work element in this project type. NULL when this is root element.|
|[Work_Element_Code](#work_element_code)|`nvarchar(3)` |The code of the work element, unique among the sibling elements within the parent work element.|
|[Work_Element_Name](#work_element_name)|`nvarchar(254)` |The name of the work element, unique among the sibling elements within the parent work element.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Full_Path](#full_path)|`nvarchar(25)` Readonly|The full path of the node in the format of dot-delimited, dot-terminated codes of the parents.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Type_Work_Element_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Parent_Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Work_Element_Code

| Property | Value |
| - | - |
|Type|nvarchar(3)|

### Work_Element_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Full_Path

| Property | Value |
| - | - |
|Type|nvarchar(25)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


