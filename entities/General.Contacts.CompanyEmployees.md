---
uid: General.Contacts.CompanyEmployees
---
# General.Contacts.CompanyEmployees Entity

**Namespace:** [General.Contacts](General.Contacts.md)  

Contains the company employee contracts. Entity: Cm_Company_Employees

## Default Visualization
Default Display Text Format:  
_{Person.PartyName:T}_  
Default Search Member:  
__  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Persons](General.Contacts.Persons.md)  
Aggregate Root:  
[General.Contacts.Persons](General.Contacts.Persons.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [ContractCode](General.Contacts.CompanyEmployees.md#contractcode) | string (16) __nullable__ | Contract number or code, unique within the company. One employee can have more than one contract. `Filter(eq)` 
| [ContractEndDate](General.Contacts.CompanyEmployees.md#contractenddate) | datetime __nullable__ | End date of the employee contract, null if the contract is still valid. `Filter(ge;le)` 
| [ContractStartDate](General.Contacts.CompanyEmployees.md#contractstartdate) | datetime __nullable__ | Start date of the employee contract. Null if it is unkown. `Filter(ge;le)` 
| [Id](General.Contacts.CompanyEmployees.md#id) | guid |  
| [Notes](General.Contacts.CompanyEmployees.md#notes) | string (254) __nullable__ | Notes for this CompanyEmployee. 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [Company](General.Contacts.CompanyEmployees.md#company) | [Companies](General.Contacts.Companies.md) | The company for which this employee works. `Required` `Filter(multi eq)` |
| [CompanyDepartment](General.Contacts.CompanyEmployees.md#companydepartment) | [CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable) | The department in which this employee is working. null means this information is unknown. `Filter(multi eq)` |
| [Person](General.Contacts.CompanyEmployees.md#person) | [Persons](General.Contacts.Persons.md) | The personal data of the employee. `Required` `Filter(multi eq)` `Owner` |


## Attribute Details

### ContractCode

Contract number or code, unique within the company. One employee can have more than one contract. `Filter(eq)`

_Type_: **string (16) __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  

### ContractEndDate

End date of the employee contract, null if the contract is still valid. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ContractStartDate

Start date of the employee contract. Null if it is unkown. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### Notes

Notes for this CompanyEmployee.

_Type_: **string (254) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  
_Maximum Length_: **254**  


## Reference Details

### Company

The company for which this employee works. `Required` `Filter(multi eq)`

_Type_: **[Companies](General.Contacts.Companies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### CompanyDepartment

The department in which this employee is working. null means this information is unknown. `Filter(multi eq)`

_Type_: **[CompanyDepartments](General.Contacts.CompanyDepartments.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

The personal data of the employee. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  



## Business Rules

[!list limit=1000 erp.entity=General.Contacts.CompanyEmployees erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=General.Contacts.CompanyEmployees erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/General_Contacts_CompanyEmployees?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#General_Contacts_CompanyEmployees?$top=10>

