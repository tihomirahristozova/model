---
uid: General.Contacts.CompanyEmployees
---
# General.Contacts.CompanyEmployees

Contains the company employee contracts. Entity: Cm_Company_Employees

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContractCode](General.Contacts.CompanyEmployees.md#contractcode) | string (nullable) | Contract number or code, unique within the company. One employee can have more than one contract. [Filter(eq)] 
| [ContractEndDate](General.Contacts.CompanyEmployees.md#contractenddate) | datetime (nullable) | End date of the employee contract, null if the contract is still valid. [Filter(ge;le)] 
| [ContractStartDate](General.Contacts.CompanyEmployees.md#contractstartdate) | datetime (nullable) | Start date of the employee contract. Null if it is unkown. [Filter(ge;le)] 
| [Id](General.Contacts.CompanyEmployees.md#id) | guid |  
| [Notes](General.Contacts.CompanyEmployees.md#notes) | string (nullable) | Notes for this CompanyEmployee. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Company](General.Contacts.CompanyEmployees.md#company) | [General.Contacts.Companies](General.Contacts.Companies.md) | The company for which this employee works. [Required] [Filter(multi eq)] |
| [CompanyDepartment](General.Contacts.CompanyEmployees.md#companydepartment) | [General.Contacts.CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable) | The department in which this employee is working. null means this information is unknown. [Filter(multi eq)] |
| [Person](General.Contacts.CompanyEmployees.md#person) | [General.Contacts.Persons](General.Contacts.Persons.md) | The personal data of the employee. [Required] [Filter(multi eq)] [Owner] |


## Attribute Details

### ContractCode

> Contract number or code, unique within the company. One employee can have more than one contract. [Filter(eq)]

_Type_: **string (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  

### ContractEndDate

> End date of the employee contract, null if the contract is still valid. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ContractStartDate

> Start date of the employee contract. Null if it is unkown. [Filter(ge;le)]

_Type_: **datetime (nullable)**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

> Notes for this CompanyEmployee.

_Type_: **string (nullable)**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  


## Reference Details

### Company

> The company for which this employee works. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.Companies](General.Contacts.Companies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### CompanyDepartment

> The department in which this employee is working. null means this information is unknown. [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

> The personal data of the employee. [Required] [Filter(multi eq)] [Owner]

_Type_: **[General.Contacts.Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=General.Contacts.CompanyEmployees erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=General.Contacts.CompanyEmployees erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=General.Contacts.CompanyEmployees erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_CompanyEmployees?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_CompanyEmployees?$top=10>

