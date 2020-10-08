---
uid: Crm.Pos.Locations
---
# Crm.Pos.Locations

Defines a company location as POS enabled location. Entity: Pos_Locations (Introduced in version 19.1.100.0)

## Attributes

| Name | Type | Description |
| ---- | ---- | --- |
| [Id](Crm.Pos.Locations.md#id) | guid |  
| [IsActive](Crm.Pos.Locations.md#isactive) | boolean (nullable) | Indicates whether the POS location is currently active and can be chosen in drop-downs, etc. [Default(true)] [Filter(eq)] 
| [PosLocationCode](Crm.Pos.Locations.md#poslocationcode) | string | Unique (with the enterprise company) code of this POS location. [Required] [Filter(multi eq;like)] 

## References

| Name | Type | Description |
| ---- | ---- | --- |
| [EnterpriseCompany](Crm.Pos.Locations.md#enterprisecompany) | [General.EnterpriseCompanies](General.EnterpriseCompanies.md) | The enterprise company of the POS location. [Required] [Filter(multi eq)] |
| [EnterpriseCompanyLocation](Crm.Pos.Locations.md#enterprisecompanylocation) | [General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md) | The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location. [Required] [Filter(multi eq)] |


## Attribute Details

### Id

_Type_: **guid**  
_Supported Filters_: **Equals, EqualsIn**  
_Default Value_: **NewGuid**  

### IsActive

> Indicates whether the POS location is currently active and can be chosen in drop-downs, etc. [Default(true)] [Filter(eq)]

_Type_: **boolean (nullable)**  
_Supported Filters_: **Equals**  
_Supports Order By_: **False**  
_Default Value_: **True**  

### PosLocationCode

> Unique (with the enterprise company) code of this POS location. [Required] [Filter(multi eq;like)]

_Type_: **string**  
_Supported Filters_: **Equals, Like, EqualsIn**  
_Supports Order By_: **False**  


## Reference Details

### EnterpriseCompany

> The enterprise company of the POS location. [Required] [Filter(multi eq)]

_Type_: **[General.EnterpriseCompanies](General.EnterpriseCompanies.md)**  
_Supported Filters_: **Equals, EqualsIn**  

### EnterpriseCompanyLocation

> The enterprise company location of the POS location. Currently, only one POS location is allowed for each company location. [Required] [Filter(multi eq)]

_Type_: **[General.Contacts.CompanyLocations](General.Contacts.CompanyLocations.md)**  
_Supported Filters_: **Equals, EqualsIn**  



## Business Rules

[!list erp.entity=Crm.Pos.Locations erp.type=business-rule default-text="None"]

## Front-End Business Rules

[!list erp.entity=Crm.Pos.Locations erp.type=front-end-business-rule default-text="None"]

## Generations

[!list erp.entity=Crm.Pos.Locations erp.type=generation default-text="None"]

## API

Domain API Query:
<https://demodb.my.erp.net/api/domain/odata/Crm_Pos_Locations?$top=10>

Domain API Query Builder:
<https://demodb.my.erp.net/api/domain/querybuilder#Crm_Pos_Locations?$top=10>

