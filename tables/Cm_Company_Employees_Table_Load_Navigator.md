# Query Cm_Company_Employees_Table_Load_Navigator


## Summary

| Name | Type | Description |
| - | - | --- |
|[Company_Employee_Id](#company_employee_id)|`uniqueidentifier` `PK`||
|[Company_Id](#company_id)|`uniqueidentifier` |The company for which this employee works.|
|[Contract_Code](#contract_code)|`nvarchar` |Contract number or code, unique within the company. One employee can have more than one contract|
|[Company_Department_Id](#company_department_id)|`uniqueidentifier` |The department in which this employee is working. NULL means this information is unknown|
|[Person_Id](#person_id)|`uniqueidentifier` |The personal data of the employee.|
|[Notes](#notes)|`nvarchar` ||
|[Contract_Start_Date](#contract_start_date)|`datetime` |Start date of the employee contract. Null if it is unkown.|
|[Contract_End_Date](#contract_end_date)|`datetime` |End date of the employee contract, null if the contract is still valid.|
|[Parent_Party_Id](#parent_party_id)|`uniqueidentifier` |Organizational unit (branch from the hierarchy of all parties) to which this party is referred to|

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
|Type|nvarchar|

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
|Type|nvarchar|

### Contract_Start_Date

| Property | Value |
| - | - |
|Type|datetime|

### Contract_End_Date

| Property | Value |
| - | - |
|Type|datetime|

### Parent_Party_Id

| Property | Value |
| - | - |
|Type|uniqueidentifier|


