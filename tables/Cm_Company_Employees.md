# Table Cm_Company_Employees

Contains the company employee contracts. Entity: Cm_Company_Employees

## Owner Tables Hierarchy

* [Cm_Persons](Cm_Persons.md)
* [Gen_Parties](Gen_Parties.md)

## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Employee_Id](#company_employee_id)|`uniqueidentifier` `PK`||
|[Company_Id](#company_id)|`uniqueidentifier` |The company for which this employee works.|
|[Contract_Code](#contract_code)|`nvarchar(16)` |Contract number or code, unique within the company. One employee can have more than one contract|
|[Company_Department_Id](#company_department_id)|`uniqueidentifier` |The department in which this employee is working. NULL means this information is unknown|
|[Person_Id](#person_id)|`uniqueidentifier` |The personal data of the employee.|
|[Notes](#notes)|`nvarchar(254)` ||
|[Contract_Start_Date](#contract_start_date)|`datetime` |Start date of the employee contract. Null if it is unkown.|
|[Contract_End_Date](#contract_end_date)|`datetime` |End date of the employee contract, null if the contract is still valid.|
|[Row_Version](#row_version)|`timestamp` ||

## Columns

### Company_Employee_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Company_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Contract_Code

| Property | Value |
| - | - |
|Type|nvarchar(16)|

### Company_Department_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Person_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|

### Notes

| Property | Value |
| - | - |
|Type|nvarchar(254)|

### Contract_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Contract_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Row_Version

| Property | Value |
| - | - |
|Type|timestamp|


