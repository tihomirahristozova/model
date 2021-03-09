# Table Prj_Types

Contains the types of projects, which can be executed by the enterprise company. Entity: Prj_Types

## Summary

| Name | Type | Description |
| - | - | --- |
|[Project_Type_Id](#project_type_id)|`uniqueidentifier` `PK`||
|[Enterprise_Company_Id](#enterprise_company_id)|`uniqueidentifier` |When not NULL means that the project type is specific to the enterprise company|
|[Project_Type_Name](#project_type_name)|`nvarchar(254)` |The name of the project type.|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Project_Type_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Enterprise_Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Project_Type_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


