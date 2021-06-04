---
uid: General.Contacts.CompanyDepartments
---
# General.Contacts.CompanyDepartments Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Hierarchical structure of the company departments. The departments and divisions are parallel and different structuring mechanisms for the companies. Entity: Cm_Company_Departments

## Default Visualization
Default Display Text Format:  
_{DepartmentName:T}_  
Default Search Member:  
_DepartmentName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Companies](General.Contacts.Companies.md)  
Aggregate Root:  
[General.Contacts.Companies](General.Contacts.Companies.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [DepartmentName](General.Contacts.CompanyDepartments.md#departmentname) | string (254) | The name of the department. `Required` `Filter(like)` 
| [Id](General.Contacts.CompanyDepartments.md#id) | guid |  
| [Notes](General.Contacts.CompanyDepartments.md#notes) | string (max) __nullable__ | Notes for this CompanyDepartment. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Company](General.Contacts.CompanyDepartments.md#company) | [Companies](General.Contacts.Companies.md) | The `Company`(General.Contacts.CompanyDepartments.md#company) to which this CompanyDepartment belongs. `Required` `Filter(multi eq)` `Owner` |
| [Parent](General.Contacts.CompanyDepartments.md#parent) | [CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable) | The parent department. null if this is root department in the company. `Filter(multi eq)` |


## Attribute Details

### DepartmentName

The name of the department. `Required` `Filter(like)`

_Type_: **string (254)**  
_Supported Filters_: **Like**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this CompanyDepartment.

_Type_: **string (max) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **2147483647**  


## Reference Details

### Company

The `Company`(General.Contacts.CompanyDepartments.md#company) to which this CompanyDepartment belongs. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Companies](General.Contacts.Companies.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_Can filter by attributes of referenced entity_: **True**  

### Parent

The parent department. null if this is root department in the company. `Filter(multi eq)`

_Type_: **[CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.CompanyDepartments erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.CompanyDepartments erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_CompanyDepartments?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_CompanyDepartments?$top=10>

