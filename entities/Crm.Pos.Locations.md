---
uid: Crm.Pos.Locations
---
# Crm.Pos.Locations Entity

**Namespace:** [Crm.Pos](Crm.Pos.md)  

Defines a company location as POS enabled location. Entity: Pos_Locations (Introduced in version 19.1)

## Default Visualization
Default Display Text Format:  
_{PosLocationCode}_  
Default Search Member:  
_PosLocationCode_  

## Aggregate
An [aggregate](https://docs.erp.net/tech/advanced/concepts/aggregates.html) is a cluster of domain objects that can be treated as a single unit.  

Aggregate Tree  
* [Crm.Pos.Locations](Crm.Pos.Locations.md)  

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Locations.md#id) | guid |  
| [IsActive](Crm.Pos.Locations.md#isactive) | boolean __nullable__ | Indicates whether the POS location is currently active and can be chosen in drop-downs, etc. `Default(true)` `Filter(eq)` 
| [PosLocationCode](Crm.Pos.Locations.md#poslocationcode) | string (16) | Unique (with the enterprise company) code of this POS location. `Required` `Filter(multi eq;like)` 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.Pos.Locations.md#enterprisecompany) | [EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company of the POS location. `Required` `Filter(multi eq)` |
| [EnterpriseCompanyLocation](Crm.Pos.Locations.md#enterprisecompanylocation) | [CompanyLocations](General.Contacts.CompanyLocations.md) | The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location. `Required` `Filter(multi eq)` |


## Attribute Details

### Id

_Type_: **guid**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

Indicates whether the POS location is currently active and can be chosen in drop-downs, etc. `Default(true)` `Filter(eq)`

_Type_: **boolean __nullable__**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PosLocationCode

Unique (with the enterprise company) code of this POS location. `Required` `Filter(multi eq;like)`

_Type_: **string (16)**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  
_Maximum Length_: **16**  


## Reference Details

### EnterpriseCompany

The enterprise company of the POS location. `Required` `Filter(multi eq)`

_Type_: **[EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location. `Required` `Filter(multi eq)`

_Type_: **[CompanyLocations](General.Contacts.CompanyLocations.md)**  
_Indexed_: **True**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list limit=1000 erp.entity=Crm.Pos.Locations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list limit=1000 erp.entity=Crm.Pos.Locations erp.type=front-end-business-rule default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Locations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Locations?$top=10>

