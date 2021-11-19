---
uid: Crm.SalesPersons
---
# Crm.SalesPersons Entity

**Namespace:** [Crm](Crm.md)  

Sales persons (or representatives) are sellers inside the enterprise company who sell the products to customers. Entity: Crm_Sales_Persons

## Default Visualization
Default Display Text Format:  
_{Person.PartyName:T}_  
Default Search Members:  
_Person.PartyName_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Parent:  
[General.Contacts.Persons](General.Contacts.Persons.md)  
Aggregate Root:  
[General.Contacts.Persons](General.Contacts.Persons.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [CommissionPercent](Crm.SalesPersons.md#commissionpercent) | decimal (7, 6) __nullable__ | The percentage (0..1) of commission percent. null means that there is no commission percent. 
| [CommissionPolicyId](Crm.SalesPersons.md#commissionpolicyid) | guid __nullable__ | Current commission policy for the sales person. null means there is no commission policy. `Filter(multi eq)` 
| [ContractEndDate](Crm.SalesPersons.md#contractenddate) | datetime __nullable__ | The ending date of the contract with the sales person. null when the sales person is still active. `Filter(ge;le)` 
| [ContractStartDate](Crm.SalesPersons.md#contractstartdate) | datetime __nullable__ | The starting date of the contract with the sales person. null when it is unknown. `Filter(ge;le)` 
| [Id](Crm.SalesPersons.md#id) | guid |  
| [IsActive](Crm.SalesPersons.md#isactive) | boolean | Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc. `Required` `Default(true)` `Filter(eq)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.SalesPersons.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable) | The Enterprise Company to which this SalesPerson applies, or null if it is for all enterprise companies. `Filter(multi eq)` |
| [EnterpriseCompanyLocation](Crm.SalesPersons.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) (nullable) | The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. null means that the sales person is not assigned to any enterprise location. `Filter(multi eq)` |
| [Person](Crm.SalesPersons.md#person) | [Persons](General.Contacts.Persons.md) | Base personal record. `Required` `Filter(multi eq)` `Owner` |
| [SalesPersonGroup](Crm.SalesPersons.md#salespersongroup) | [SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md) | The sales person group to which this sales person is assigned. `Required` `Filter(multi eq)` |


## Attribute Details

### CommissionPercent

The percentage (0..1) of commission percent. null means that there is no commission percent.

_Type_: **decimal (7, 6) __nullable__**  
_Supported Filters_: **NotFilterable**  
_Supports Order By_: **False**  

### CommissionPolicyId

Current commission policy for the sales person. null means there is no commission policy. `Filter(multi eq)`

_Type_: **guid __nullable__**  
_Supported Filters_: **Equals, EqualsIn**  

### ContractEndDate

The ending date of the contract with the sales person. null when the sales person is still active. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### ContractStartDate

The starting date of the contract with the sales person. null when it is unknown. `Filter(ge;le)`

_Type_: **datetime __nullable__**  
_Supported Filters_: **GreaterThanOrLessThan**  
_Supports Order By_: **False**  

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Specifies whether the sales person is active and should be included in the list when choosing sales person through drop-downs, lists, etc. `Required` `Default(true)` `Filter(eq)`

_Type_: **boolean**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  


## Reference Details

### EnterpriseCompany

The Enterprise Company to which this SalesPerson applies, or null if it is for all enterprise companies. `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The enterprise company location, to which the sales person is assigned. The sales person is allowed to sell to other locations, but this is the default location. null means that the sales person is not assigned to any enterprise location. `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md) (nullable)**  
_Supported Filters_: **Equals, EqualsIn**  

### Person

Base personal record. `Required` `Filter(multi eq)` `Owner`

_Type_: **[Persons](General.Contacts.Persons.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_[Filterable Reference](https://docs.erp.net/dev/domain-api/filterable-references.html)_: **True**  

### SalesPersonGroup

The sales person group to which this sales person is assigned. `Required` `Filter(multi eq)`

_Type_: **[SalesPersonGroups](Crm.Distribution.SalesPersonGroups.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.SalesPersons erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.SalesPersons erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_SalesPersons?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_SalesPersons?$top=10>

