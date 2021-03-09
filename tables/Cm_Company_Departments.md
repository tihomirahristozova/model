# Table Cm_Company_Departments

Hierarchical structure of the company departments. The departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Departments

## Owner Tables Hierarchy

* [Cm_Companies](Cm_Companies.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Department_Id](#company_department_id)|`uniqueidentifier` `PK`||
|[Company_Id](#company_id)|`uniqueidentifier` ||
|[Department_Name](#department_name)|`nvarchar(254)` |The name of the department.|
|[Parent_Company_Department_Id](#parent_company_department_id)|`uniqueidentifier` |The parent department. NULL if this is root department in the company|
|[Notes](#notes)|`nvarchar(2147483647)` ||
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Company_Department_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Department_Name

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Parent_Company_Department_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(2147483647)|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


