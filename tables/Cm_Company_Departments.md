# Table Cm_Company_Departments

Hierarchical structure of the company departments. The departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Departments

# Aggregate Hierarchy

* [Cm_Companies](Cm_Companies.md)

# Columns

| Name | Type | Value | Description |
| - | - | - | --- |
|Company_Department_Id|`Guid`|`PK`, Readonly||
|Department_Name|`String`||The name of the department. `Required` `Filter(like)` |
|Notes|`String`||Notes for this CompanyDepartment. |
